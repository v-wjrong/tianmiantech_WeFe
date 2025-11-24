# 基础信息

|      |      |
|------|------|
| 名称 | GrpcServer |
| 编码语言 | .java |
| 代码路径 | WeFe/gateway/src/main/java/com/welab/wefe/gateway/init/grpc/GrpcServer.java |
| 包名 | com.welab.wefe.gateway.init.grpc |
| 依赖项 | ['com.welab.wefe.gateway.base.GrpcServerAnnotate', 'com.welab.wefe.gateway.common.GrpcConstant', 'com.welab.wefe.gateway.common.RpcServerStatusEnum', 'com.welab.wefe.gateway.common.GrpcServerScopeEnum', 'com.welab.wefe.gateway.util.ClassUtil', 'io.grpc', 'io.grpc.netty.NettyServerBuilder', 'io.netty.handler.ssl.SslContext', 'org.apache.commons.collections4.CollectionUtils', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.util.List', 'java.util.Map', 'java.util.concurrent.TimeUnit'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| GrpcServer | class |  |



## 类 GrpcServer

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | GrpcServer |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| server | Server |  |
| useScope | GrpcServerScopeEnum |  |
| tlsEnable | boolean |  |
| sslContext | SslContext |  |
| status = RpcServerStatusEnum.SHUTDOWN | RpcServerStatusEnum |  |
| LOG = LoggerFactory.getLogger(GrpcServer.class) | Logger |  |
| port | int |  |
| name | String |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| isTlsEnable | boolean |  |
| getUseScope | GrpcServerScopeEnum |  |
| start | boolean |  |
| listToInstanceArray | ServerInterceptor[] |  |
| getPort | int |  |
| setName | void |  |
| setUseScope | void |  |
| getSslContext | SslContext |  |
| setSslContext | void |  |
| stop | void |  |
| restart | boolean |  |
| getStatus | RpcServerStatusEnum |  |
| setTlsEnable | void |  |
| setPort | void |  |
| setStatus | void |  |
| getName | String |  |




