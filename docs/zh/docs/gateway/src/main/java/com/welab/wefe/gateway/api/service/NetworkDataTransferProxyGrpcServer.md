# 基础信息

|      |      |
|------|------|
| 名称 | NetworkDataTransferProxyGrpcServer |
| 编码语言 | .java |
| 代码路径 | WeFe/gateway/src/main/java/com/welab/wefe/gateway/api/service/NetworkDataTransferProxyGrpcServer.java |
| 包名 | com.welab.wefe.gateway.api.service |
| 依赖项 | ['com.welab.wefe.gateway.api.meta.basic.BasicMetaProto', 'com.welab.wefe.gateway.api.meta.basic.GatewayMetaProto', 'com.welab.wefe.gateway.api.service.proto.NetworkDataTransferProxyServiceGrpc', 'com.welab.wefe.gateway.api.streammessage.PushDataSourceRequestStreamObserver', 'com.welab.wefe.gateway.base.GrpcServer', 'com.welab.wefe.gateway.common.GrpcServerScopeEnum', 'com.welab.wefe.gateway.interceptor.AntiTamperServerInterceptor', 'com.welab.wefe.gateway.interceptor.SignVerifyServerInterceptor', 'com.welab.wefe.gateway.interceptor.SystemTimestampVerifyServerInterceptor', 'com.welab.wefe.gateway.service.base.AbstractRecvTransferMetaService', 'com.welab.wefe.gateway.util.TransferMetaUtil', 'io.grpc.stub.StreamObserver', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.beans.factory.annotation.Autowired'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| NetworkDataTransferProxyGrpcServer | class |  |



## 类 NetworkDataTransferProxyGrpcServer

|      |      |
|------|------|
| 访问范围 | @GrpcServer(interceptors = {AntiTamperServerInterceptor.class, SignVerifyServerInterceptor.class, SystemTimestampVerifyServerInterceptor.class});public |
| 类型 | class |
| 名称 | NetworkDataTransferProxyGrpcServer |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| recvTransferMetaService | AbstractRecvTransferMetaService |  |
| LOG = LoggerFactory.getLogger(NetworkDataTransferProxyGrpcServer.class) | Logger |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| push | void |  |
| pushDataSource | StreamObserver<GatewayMetaProto.TransferMeta> |  |




