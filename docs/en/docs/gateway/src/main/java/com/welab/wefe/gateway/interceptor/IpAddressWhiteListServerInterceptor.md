# Basic Information

|      |      |
|------|------|
| Name | IpAddressWhiteListServerInterceptor |
| Language | .java |
| Code Path | WeFe/gateway/src/main/java/com/welab/wefe/gateway/interceptor/IpAddressWhiteListServerInterceptor.java |
| Package Name | com.welab.wefe.gateway.interceptor |
| Dependencies | ['com.welab.wefe.common.util.IpAddressUtil', 'com.welab.wefe.common.wefe.enums.GatewayProcessorType', 'com.welab.wefe.gateway.GatewayServer', 'com.welab.wefe.gateway.api.meta.basic.GatewayMetaProto', 'com.welab.wefe.gateway.cache.SystemConfigCache', 'com.welab.wefe.gateway.service.MessageService', 'io.grpc', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.net.InetSocketAddress', 'java.util.concurrent.atomic.AtomicInteger'] |
| Brief Description | The IpAddressWhiteListServerInterceptor is used to check whether the client's IP address is within the whitelist. If not, access is denied. It supports cache refresh and concurrency control. |

# Description

IpAddressWhiteListServerInterceptor is a gRPC-based server interceptor designed to implement IP whitelist access control. Its core functionalities include: validating client IP legitimacy by intercepting request messages, supporting both local same-subnet access and configured whitelist modes. When no whitelist is configured, only same-subnet access is permitted by default; if an IP is not in the whitelist and the maximum concurrent refresh count (3 times) hasn't been reached, it automatically refreshes the cache for revalidation. During interception, it logs unauthorized access attempts and exceptions, while saving error records via MessageService. For illegal requests, it returns a PERMISSION_DENIED status and terminates the connection, with concurrent control mechanisms implemented during cache refresh operations.

# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| IpAddressWhiteListServerInterceptor | class | The Java class `IpAddressWhiteListServerInterceptor` implements a gRPC server interceptor that checks whether the client IP is in the whitelist or the same network segment, otherwise denying access. It supports cache refresh with a maximum concurrency of 3. |



## Class IpAddressWhiteListServerInterceptor

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | IpAddressWhiteListServerInterceptor |
| Description | The Java class `IpAddressWhiteListServerInterceptor` implements a gRPC server interceptor that checks whether the client IP is in the whitelist or the same network segment, otherwise denying access. It supports cache refresh with a maximum concurrency of 3. |


### UML Class Diagram

```mermaid
classDiagram
    class AbstractServerInterceptor {
        <<Abstract>>
    }

    class IpAddressWhiteListServerInterceptor {
        -Logger LOG
        -static int MAX_REFRESH_CACHE_CONCURRENT_COUNT
        -static AtomicInteger CURRENT_CONCURRENT_COUNT
        +intercept(ServerCall~ReqT~ call, Metadata headers, ServerCallHandler~ReqT,RespT~ next) ServerCall.Listener~ReqT~
        -isValidRemoteAddr(InetSocketAddress localSocketAddress, InetSocketAddress remoteSocketAddress) boolean
        -isRefreshCacheAgain() boolean
    }

    class IpAddressUtil {
        <<Utility>>
        +getIpAddress(InetSocketAddress socketAddress) String
        +isSameNetworkSegment(InetSocketAddress localAddr, InetSocketAddress remoteAddr) boolean
    }

    class SystemConfigCache {
        -static SystemConfigCache instance
        +getInstance() SystemConfigCache
        +cacheIsEmpty() boolean
        +isExistIp(String ip) boolean
        +refreshCache() void
    }

    class MessageService {
        <<Interface>>
        +saveError(String title, String content) void
    }

    AbstractServerInterceptor <|-- IpAddressWhiteListServerInterceptor
    IpAddressWhiteListServerInterceptor --> IpAddressUtil : Uses
    IpAddressWhiteListServerInterceptor --> SystemConfigCache : Depends on
    IpAddressWhiteListServerInterceptor --> MessageService : Invokes
```

This code implements a gRPC-based IP whitelist interceptor with key functionalities: 1) Validating client IPs against a whitelist via interceptor pattern; 2) Managing whitelist configurations using SystemConfigCache; 3) Implementing cache refresh rate-limiting mechanism; 4) Logging exceptions via MessageService. The core logic resides in the isValidRemoteAddr method, which checks whether the client IP belongs to the same network segment as the server or exists in the whitelist cache, triggering cache refresh retry mechanism upon misses. The class diagram clearly illustrates inheritance relationships and critical dependency components.


### Internal Method Call Graph

```mermaid
graph TD
    A["Class IpAddressWhiteListServerInterceptor"]
    B["Property: Logger LOG"]
    C["Static Property: MAX_REFRESH_CACHE_CONCURRENT_COUNT"]
    D["Static Property: CURRENT_CONCURRENT_COUNT"]
    E["Method: intercept(ServerCall<ReqT, RespT>, Metadata, ServerCallHandler<ReqT, RespT>)"]
    F["Method: isValidRemoteAddr(InetSocketAddress, InetSocketAddress)"]
    G["Method: isRefreshCacheAgain()"]
    H["Inner Class: SimpleForwardingServerCallListener"]

    A --> B
    A --> C
    A --> D
    A --> E
    A --> F
    A --> G
    E --> H

    E1["Get local/remote Socket addresses"] --> E
    E2["Create nextListener"] --> E
    E3["Create request interceptor"] --> E
    E4["Validate IP validity"] --> E3
    E5["Handle invalid requests"] --> E4
    E6["Forward valid requests"] --> E4

    F1["Get local/remote IPs"] --> F
    F2["Check cache empty state"] --> F
    F3["Check same subnet"] --> F2
    F4["Check IP whitelist"] --> F2
    F5["Secondary cache check"] --> F4

    G1["Check concurrent count"] --> G
    G2["Refresh cache"] --> G1
    G3["Decrement counter"] --> G2
```

```mermaid
sequenceDiagram
    participant Client
    participant Interceptor as IpAddressWhiteListServerInterceptor
    participant ServerCall
    participant ServerCallHandler
    participant SystemConfigCache

    Client->>Interceptor: Send request
    Interceptor->>ServerCall: getAttributes()
    ServerCall-->>Interceptor: Return local/remote addresses
    Interceptor->>ServerCallHandler: startCall()
    ServerCallHandler-->>Interceptor: Return nextListener
    Interceptor->>Interceptor: Create reqInterceptor
    alt Message processing
        Client->>Interceptor: onMessage()
        Interceptor->>Interceptor: Validate IP validity
        alt Invalid IP
            Interceptor->>ServerCall: close()
        else Valid IP
            Interceptor->>ServerCallHandler: Forward message
        end
    end

    Note right of Interceptor: IP validation flow
    Interceptor->>IpAddressUtil: getIpAddress()
    IpAddressUtil-->>Interceptor: Return IP string
    Interceptor->>SystemConfigCache: isExistIp()
    SystemConfigCache-->>Interceptor: Return check result
    alt Cache refresh required
        Interceptor->>SystemConfigCache: refreshCache()
    end
```

This flowchart demonstrates the core logic of the IP whitelist interceptor, primarily consisting of three key methods: intercept() handles gRPC call interception, isValidRemoteAddr() verifies IP legitimacy, and isRefreshCacheAgain() controls cache refresh frequency. The sequence diagram details the complete interaction process from client request to IP validation, highlighting the decision flow of IP whitelist checks and exception handling mechanisms. The entire design ensures stability in high-concurrency scenarios through a dual-cache check mechanism while strictly adhering to whitelist access control policies.

### Field List

| Name  | Type  | Description |
|-------|-------|------|
| CURRENT_CONCURRENT_COUNT = new AtomicInteger(0) | AtomicInteger | Define a static atomic integer variable CURRENT_CONCURRENT_COUNT with an initial value of 0, used for thread-safe concurrent counting. |
| MAX_REFRESH_CACHE_CONCURRENT_COUNT = 3 | int | The static constant MAX_REFRESH_CACHE_CONCURRENT_COUNT has a value of 3, which limits the maximum concurrency count for cache refresh. |
| LOG = LoggerFactory.getLogger(IpAddressWhiteListServerInterceptor.class) | Logger | The class IpAddressWhiteListServerInterceptor defines a private immutable logger LOG. |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| isValidRemoteAddr | boolean | Check if the client IP is valid: If no whitelist is set, it must be in the same network segment; if it matches the server IP, it is allowed; otherwise, check the whitelist—if not listed, reject and log the error. |
| intercept | ServerCall.Listener<ReqT> | This method intercepts gRPC requests and verifies whether the client IP is legitimate. If the IP is invalid or an exception occurs, it logs the event and closes the connection; otherwise, it proceeds with processing the request. |
| isRefreshCacheAgain | boolean | Method checks whether the current number of concurrent cache refresh requests has not exceeded the limit. If not, it refreshes the cache and returns success; otherwise, it logs the event and returns failure. |




