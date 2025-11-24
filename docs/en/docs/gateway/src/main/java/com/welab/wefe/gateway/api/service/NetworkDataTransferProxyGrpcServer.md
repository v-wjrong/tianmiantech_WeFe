# Basic Information

|      |      |
|------|------|
| Name | NetworkDataTransferProxyGrpcServer |
| Language | .java |
| Code Path | WeFe/gateway/src/main/java/com/welab/wefe/gateway/api/service/NetworkDataTransferProxyGrpcServer.java |
| Package Name | com.welab.wefe.gateway.api.service |
| Dependencies | ['com.welab.wefe.gateway.api.meta.basic.BasicMetaProto', 'com.welab.wefe.gateway.api.meta.basic.GatewayMetaProto', 'com.welab.wefe.gateway.api.service.proto.NetworkDataTransferProxyServiceGrpc', 'com.welab.wefe.gateway.api.streammessage.PushDataSourceRequestStreamObserver', 'com.welab.wefe.gateway.base.GrpcServer', 'com.welab.wefe.gateway.common.GrpcServerScopeEnum', 'com.welab.wefe.gateway.interceptor.AntiTamperServerInterceptor', 'com.welab.wefe.gateway.interceptor.SignVerifyServerInterceptor', 'com.welab.wefe.gateway.interceptor.SystemTimestampVerifyServerInterceptor', 'com.welab.wefe.gateway.service.base.AbstractRecvTransferMetaService', 'com.welab.wefe.gateway.util.TransferMetaUtil', 'io.grpc.stub.StreamObserver', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.beans.factory.annotation.Autowired'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| NetworkDataTransferProxyGrpcServer | class |  |



## Class NetworkDataTransferProxyGrpcServer

|      |      |
|------|------|
| Access Modifier | @GrpcServer(interceptors = {AntiTamperServerInterceptor.class, SignVerifyServerInterceptor.class, SystemTimestampVerifyServerInterceptor.class});public |
| Type | class |
| Name | NetworkDataTransferProxyGrpcServer |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| recvTransferMetaService | AbstractRecvTransferMetaService |  |
| LOG = LoggerFactory.getLogger(NetworkDataTransferProxyGrpcServer.class) | Logger |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| push | void |  |
| pushDataSource | StreamObserver<GatewayMetaProto.TransferMeta> |  |




