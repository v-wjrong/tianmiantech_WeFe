# Basic Information

|      |      |
|------|------|
| Name | AbstractServerInterceptor |
| Language | .java |
| Code Path | WeFe/gateway/src/main/java/com/welab/wefe/gateway/interceptor/AbstractServerInterceptor.java |
| Package Name | com.welab.wefe.gateway.interceptor |
| Dependencies | ['com.welab.wefe.common.util.IpAddressUtil', 'com.welab.wefe.gateway.GatewayServer', 'com.welab.wefe.gateway.base.GrpcServerAnnotate', 'com.welab.wefe.gateway.common.GrpcConstant', 'com.welab.wefe.gateway.service.MessageService', 'io.grpc', 'org.springframework.util.CollectionUtils', 'java.net.InetSocketAddress', 'java.util.ArrayList', 'java.util.List', 'java.util.Map'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| AbstractServerInterceptor | class |  |



## Class AbstractServerInterceptor

|      |      |
|------|------|
| Access Modifier | public abstract |
| Type | class |
| Name | AbstractServerInterceptor |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| excludeInterceptMethods = new ArrayList<>() | List<String> |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| interceptCall | ServerCall.Listener<ReqT> |  |
| intercept | ServerCall.Listener<ReqT> |  |
| saveSignVerifyFailInfo | void |  |
| getExcludeInterceptMethods | List<String> |  |
| isInterceptTarget | boolean |  |
| isReqInvalid | boolean |  |
| setReqInvalid | void |  |
| getClientIpAddr | String |  |
| setExcludeInterceptMethods | void |  |




