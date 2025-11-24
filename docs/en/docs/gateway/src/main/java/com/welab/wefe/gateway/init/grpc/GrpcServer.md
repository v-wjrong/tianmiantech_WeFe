# Basic Information

|      |      |
|------|------|
| Name | GrpcServer |
| Language | .java |
| Code Path | WeFe/gateway/src/main/java/com/welab/wefe/gateway/init/grpc/GrpcServer.java |
| Package Name | com.welab.wefe.gateway.init.grpc |
| Dependencies | ['com.welab.wefe.gateway.base.GrpcServerAnnotate', 'com.welab.wefe.gateway.common.GrpcConstant', 'com.welab.wefe.gateway.common.RpcServerStatusEnum', 'com.welab.wefe.gateway.common.GrpcServerScopeEnum', 'com.welab.wefe.gateway.util.ClassUtil', 'io.grpc', 'io.grpc.netty.NettyServerBuilder', 'io.netty.handler.ssl.SslContext', 'org.apache.commons.collections4.CollectionUtils', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.util.List', 'java.util.Map', 'java.util.concurrent.TimeUnit'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| GrpcServer | class |  |



## Class GrpcServer

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | GrpcServer |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| server | Server |  |
| useScope | GrpcServerScopeEnum |  |
| tlsEnable | boolean |  |
| sslContext | SslContext |  |
| status = RpcServerStatusEnum.SHUTDOWN | RpcServerStatusEnum |  |
| LOG = LoggerFactory.getLogger(GrpcServer.class) | Logger |  |
| port | int |  |
| name | String |  |

### Method List

| Name  | Type  | Description |
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




