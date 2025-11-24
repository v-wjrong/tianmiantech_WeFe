# Basic Information

|      |      |
|------|------|
| Name | NetworkDataTransferProxyServiceGrpc |
| Language | .java |
| Code Path | WeFe/gateway/src/main/java/com/welab/wefe/gateway/api/service/proto/NetworkDataTransferProxyServiceGrpc.java |
| Package Name | com.welab.wefe.gateway.api.service.proto |
| Dependencies | ['io.grpc.MethodDescriptor.generateFullMethodName', 'io.grpc.stub.ClientCalls.asyncBidiStreamingCall', 'io.grpc.stub.ClientCalls.asyncUnaryCall', 'io.grpc.stub.ClientCalls', 'io.grpc.stub.ServerCalls.asyncBidiStreamingCall', 'io.grpc.stub.ServerCalls.asyncUnaryCall', 'io.grpc.stub.ServerCalls'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| NetworkDataTransferProxyServiceGrpc | class |  |



## Class NetworkDataTransferProxyServiceGrpc

|      |      |
|------|------|
| Access Modifier | @javax.annotation.Generated(;    value = "by gRPC proto compiler (version 1.29.0)",;    comments = "Source: gateway-service.proto");public final |
| Type | class |
| Name | NetworkDataTransferProxyServiceGrpc |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| METHODID_PUSH = 0 | int |  |
| SERVICE_NAME = "com.welab.wefe.gateway.api.service.proto.NetworkDataTransferProxyService" | String |  |
| serviceDescriptor | io.grpc.ServiceDescriptor |  |
| getPushMethod | io.grpc.MethodDescriptor<com.welab.wefe.gateway.api.meta.basic.GatewayMetaProto.TransferMeta,
      com.welab.wefe.gateway.api.meta.basic.BasicMetaProto.ReturnStatus> |  |
| METHODID_PUSH_DATA_SOURCE = 1 | int |  |
| getPushDataSourceMethod | io.grpc.MethodDescriptor<com.welab.wefe.gateway.api.meta.basic.GatewayMetaProto.TransferMeta,
      com.welab.wefe.gateway.api.meta.basic.GatewayMetaProto.TransferMeta> |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getPushMethod | io.grpc.MethodDescriptor<com.welab.wefe.gateway.api.meta.basic.GatewayMetaProto.TransferMeta,
      com.welab.wefe.gateway.api.meta.basic.BasicMetaProto.ReturnStatus> |  |
| newStub | NetworkDataTransferProxyServiceStub |  |
| getPushDataSourceMethod | io.grpc.MethodDescriptor<com.welab.wefe.gateway.api.meta.basic.GatewayMetaProto.TransferMeta,
      com.welab.wefe.gateway.api.meta.basic.GatewayMetaProto.TransferMeta> |  |
| newBlockingStub | NetworkDataTransferProxyServiceBlockingStub |  |
| newFutureStub | NetworkDataTransferProxyServiceFutureStub |  |
| getServiceDescriptor | io.grpc.ServiceDescriptor |  |




