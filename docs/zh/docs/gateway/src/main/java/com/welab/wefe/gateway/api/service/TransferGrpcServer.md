# 基础信息

|      |      |
|------|------|
| 名称 | TransferGrpcServer |
| 编码语言 | .java |
| 代码路径 | WeFe/gateway/src/main/java/com/welab/wefe/gateway/api/service/TransferGrpcServer.java |
| 包名 | com.welab.wefe.gateway.api.service |
| 依赖项 | ['com.welab.wefe.gateway.api.meta.basic.BasicMetaProto', 'com.welab.wefe.gateway.api.meta.basic.GatewayMetaProto', 'com.welab.wefe.gateway.api.service.proto.TransferServiceGrpc', 'com.welab.wefe.gateway.base.GrpcServer', 'com.welab.wefe.gateway.common.GrpcServerScopeEnum', 'com.welab.wefe.gateway.interceptor.IpAddressWhiteListServerInterceptor', 'com.welab.wefe.gateway.service.base.AbstractRecvTransferMetaService', 'com.welab.wefe.gateway.service.base.AbstractSendTransferMetaService', 'com.welab.wefe.gateway.util.TransferMetaUtil', 'io.grpc.stub.StreamObserver', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.beans.factory.annotation.Autowired'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| TransferGrpcServer | class |  |



## 类 TransferGrpcServer

|      |      |
|------|------|
| 访问范围 | @GrpcServer(useScope = GrpcServerScopeEnum.INTERNAL, interceptors = {IpAddressWhiteListServerInterceptor.class});public |
| 类型 | class |
| 名称 | TransferGrpcServer |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| LOG = LoggerFactory.getLogger(TransferGrpcServer.class) | Logger |  |
| recvTransferMetaService | AbstractRecvTransferMetaService |  |
| sendTransferMetaService | AbstractSendTransferMetaService |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| send | void |  |
| recv | void |  |
| checkStatusNow | void |  |




