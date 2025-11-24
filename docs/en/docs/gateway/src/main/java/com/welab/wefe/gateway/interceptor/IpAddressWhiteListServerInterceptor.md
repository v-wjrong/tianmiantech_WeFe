# Basic Information

|      |      |
|------|------|
| Name | IpAddressWhiteListServerInterceptor |
| Language | .java |
| Code Path | WeFe/gateway/src/main/java/com/welab/wefe/gateway/interceptor/IpAddressWhiteListServerInterceptor.java |
| Package Name | com.welab.wefe.gateway.interceptor |
| Dependencies | ['com.welab.wefe.common.util.IpAddressUtil', 'com.welab.wefe.common.wefe.enums.GatewayProcessorType', 'com.welab.wefe.gateway.GatewayServer', 'com.welab.wefe.gateway.api.meta.basic.GatewayMetaProto', 'com.welab.wefe.gateway.cache.SystemConfigCache', 'com.welab.wefe.gateway.service.MessageService', 'io.grpc', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.net.InetSocketAddress', 'java.util.concurrent.atomic.AtomicInteger'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| IpAddressWhiteListServerInterceptor | class |  |



## Class IpAddressWhiteListServerInterceptor

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | IpAddressWhiteListServerInterceptor |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| CURRENT_CONCURRENT_COUNT = new AtomicInteger(0) | AtomicInteger |  |
| LOG = LoggerFactory.getLogger(IpAddressWhiteListServerInterceptor.class) | Logger |  |
| MAX_REFRESH_CACHE_CONCURRENT_COUNT = 3 | int |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| intercept | ServerCall.Listener<ReqT> |  |
| isValidRemoteAddr | boolean |  |
| isRefreshCacheAgain | boolean |  |




