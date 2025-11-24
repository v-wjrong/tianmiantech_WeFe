# 基础信息

|      |      |
|------|------|
| 名称 | AbstractServerInterceptor |
| 编码语言 | .java |
| 代码路径 | WeFe/gateway/src/main/java/com/welab/wefe/gateway/interceptor/AbstractServerInterceptor.java |
| 包名 | com.welab.wefe.gateway.interceptor |
| 依赖项 | ['com.welab.wefe.common.util.IpAddressUtil', 'com.welab.wefe.gateway.GatewayServer', 'com.welab.wefe.gateway.base.GrpcServerAnnotate', 'com.welab.wefe.gateway.common.GrpcConstant', 'com.welab.wefe.gateway.service.MessageService', 'io.grpc', 'org.springframework.util.CollectionUtils', 'java.net.InetSocketAddress', 'java.util.ArrayList', 'java.util.List', 'java.util.Map'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| AbstractServerInterceptor | class |  |



## 类 AbstractServerInterceptor

|      |      |
|------|------|
| 访问范围 | public abstract |
| 类型 | class |
| 名称 | AbstractServerInterceptor |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| excludeInterceptMethods = new ArrayList<>() | List<String> |  |

### 方法列表

| 名称  | 类型  | 说明 |
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




