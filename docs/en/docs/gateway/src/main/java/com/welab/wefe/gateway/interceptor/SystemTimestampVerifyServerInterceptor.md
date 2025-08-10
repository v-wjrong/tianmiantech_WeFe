# Basic Information

|      |      |
|------|------|
| Name | SystemTimestampVerifyServerInterceptor |
| Language | .java |
| Code Path | WeFe/gateway/src/main/java/com/welab/wefe/gateway/interceptor/SystemTimestampVerifyServerInterceptor.java |
| Package Name | com.welab.wefe.gateway.interceptor |
| Dependencies | ['com.welab.wefe.common.util.DateUtil', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.gateway.GatewayServer', 'com.welab.wefe.gateway.api.meta.basic.GatewayMetaProto', 'com.welab.wefe.gateway.common.GrpcConstant', 'com.welab.wefe.gateway.service.MessageService', 'io.grpc', 'org.apache.commons.lang3.math.NumberUtils', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.util.Date'] |
| Brief Description | This is a gRPC server interceptor designed to validate whether the client request timestamp is valid. It checks if the timestamp is empty or exceeds the threshold difference from the server time, rejecting the request and logging an error if invalid. |

# Description

The `SystemTimestampVerifyServerInterceptor` is a gRPC server-side interceptor designed to validate the system timestamp in client requests. It checks whether the timestamp in the request header is empty and verifies if the time difference between the client and server exceeds the predefined maximum value (`GrpcConstant.MAX_SYSTEM_TIMESTAMP_DIFF`). If validation fails, it logs an error and saves the error message via the `MessageService`, then returns a `FAILED_PRECONDITION` status. This interceptor specifically handles potential underscore-related issues in request headers when forwarded through nginx.

# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| SystemTimestampVerifyServerInterceptor | class | This is a gRPC server interceptor designed to validate the timestamp submitted by clients. It checks whether the timestamp is empty or exceeds a threshold deviation from the server time, rejecting the request and logging an error if invalid. |



## Class SystemTimestampVerifyServerInterceptor

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | SystemTimestampVerifyServerInterceptor |
| Description | This is a gRPC server interceptor designed to validate the timestamp submitted by clients. It checks whether the timestamp is empty or exceeds a threshold deviation from the server time, rejecting the request and logging an error if invalid. |


### UML Class Diagram

```mermaid
classDiagram
    class AbstractServerInterceptor {
        <<Abstract>>
    }
    class SystemTimestampVerifyServerInterceptor {
        -Logger LOG
        +intercept(ServerCall~ReqT~ call, Metadata headers, ServerCallHandler~ReqT,RespT~ next) ServerCall.Listener~ReqT~
    }
    class ServerCall~ReqT,RespT~ {
        <<Interface>>
        +close(Status status, Metadata trailers)
    }
    class ServerCallHandler~ReqT,RespT~ {
        <<Interface>>
        +startCall(ServerCall~ReqT~ call, Metadata headers) ServerCall.Listener~ReqT~
    }
    class ForwardingServerCallListener~ReqT~ {
        <<Abstract>>
    }
    class SimpleForwardingServerCallListener~ReqT~ {
        -ServerCall.Listener~ReqT~ delegate
        +onMessage(ReqT message)
    }
    class GatewayServer {
        +CONTEXT: ApplicationContext
    }
    class MessageService {
        <<Interface>>
        +saveError(String title, String content)
    }

    SystemTimestampVerifyServerInterceptor --|> AbstractServerInterceptor
    SimpleForwardingServerCallListener --|> ForwardingServerCallListener
    SystemTimestampVerifyServerInterceptor --> ServerCall : depends
    SystemTimestampVerifyServerInterceptor --> ServerCallHandler : depends
    SystemTimestampVerifyServerInterceptor --> SimpleForwardingServerCallListener : creates
    SystemTimestampVerifyServerInterceptor --> GatewayServer : depends
    SystemTimestampVerifyServerInterceptor --> MessageService : depends
```

Class diagram description: This diagram illustrates the inheritance and dependency relationships of the SystemTimestampVerifyServerInterceptor class. It inherits from AbstractServerInterceptor and implements gRPC server interceptor functionality, primarily validating the timestamp submitted by clients. It depends on the ServerCall and ServerCallHandler interfaces to handle gRPC calls, uses SimpleForwardingServerCallListener to intercept request messages, and logs error information through GatewayServer and MessageService. The core logic for timestamp validation and exception handling is implemented in the intercept method.


### Internal Method Call Graph

```mermaid
graph TD
    A["SystemTimestampVerifyServerInterceptor"]
    B["intercept(ServerCall<ReqT, RespT> call, Metadata headers, ServerCallHandler<ReqT, RespT> next)"]
    C["Get client timestamp: headers.get(GrpcConstant.SYSTEM_TIMESTAMP_HEADER_KEY)"]
    D["Create listener: next.startCall(call, headers)"]
    E["Build intercept listener: SimpleForwardingServerCallListener<ReqT>"]
    F["onMessage(ReqT message)"]
    G["Parse TransferMeta to get memberName"]
    H{"Check if clientTimestampStr is empty?"}
    I["Log error: 'Timestamp is empty' and mark reqInvalid"]
    J["Convert timestamp to long: NumberUtils.toLong"]
    K{"Check if time difference exceeds threshold?"}
    L["Log error: 'Time difference exceeds limit' and mark reqInvalid"]
    M["Catch exception and log error"]
    N{"Is reqInvalid true?"}
    O["Close call: call.close(Status.FAILED_PRECONDITION)"]
    P["Continue processing: super.onMessage(message)"]

    A --> B
    B --> C
    B --> D
    B --> E
    E --> F
    F --> G
    F --> H
    H -->|Yes| I
    H -->|No| J
    J --> K
    K -->|Yes| L
    K -->|No| P
    F -.->|Exception| M
    M --> I
    I --> N
    L --> N
    N -->|Yes| O
    N -->|No| P
```

This code implements a gRPC server interceptor to validate the system timestamp in client requests. The main workflow includes: retrieving the client timestamp header, creating a message listener, checking whether the timestamp is empty or exceeds the threshold difference from server time (configured via GrpcConstant.MAX_SYSTEM_TIMESTAMP_DIFF) upon message arrival. If validation fails, it logs error messages and terminates the request; otherwise, it proceeds with subsequent processing. The entire process incorporates exception handling and multiple error scenario management to ensure system time synchronization security.

### Field List

| Name  | Type  | Description |
|-------|-------|------|
| LOG = LoggerFactory.getLogger(SystemTimestampVerifyServerInterceptor.class) | Logger | The class SystemTimestampVerifyServerInterceptor defines a private static log object LOG for logging purposes. |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| intercept | ServerCall.Listener<ReqT> | The gRPC interceptor validates the client timestamp, checking if it is empty or exceeds the allowable time difference from the server time. If invalid, the request is rejected and an error is logged. |




