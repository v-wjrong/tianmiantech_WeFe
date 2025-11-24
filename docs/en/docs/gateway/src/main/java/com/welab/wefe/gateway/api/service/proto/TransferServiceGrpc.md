# Basic Information

|      |      |
|------|------|
| Name | TransferServiceGrpc |
| Language | .java |
| Code Path | WeFe/gateway/src/main/java/com/welab/wefe/gateway/api/service/proto/TransferServiceGrpc.java |
| Package Name | com.welab.wefe.gateway.api.service.proto |
| Dependencies | ['io.grpc.MethodDescriptor.generateFullMethodName', 'io.grpc.stub.ClientCalls.asyncUnaryCall', 'io.grpc.stub.ClientCalls.blockingUnaryCall', 'io.grpc.stub.ClientCalls.futureUnaryCall', 'io.grpc.stub.ServerCalls.asyncUnaryCall', 'io.grpc.stub.ServerCalls.asyncUnimplementedUnaryCall'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| TransferServiceGrpc | class |  |



## Class TransferServiceGrpc

|      |      |
|------|------|
| Access Modifier | @javax.annotation.Generated(;    value = "by gRPC proto compiler (version 1.29.0)",;    comments = "Source: gateway-service.proto");public final |
| Type | class |
| Name | TransferServiceGrpc |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| METHODID_RECV = 1 | int |  |
| getCheckStatusNowMethod | io.grpc.MethodDescriptor<com.welab.wefe.gateway.api.meta.basic.GatewayMetaProto.TransferMeta,
      com.welab.wefe.gateway.api.meta.basic.GatewayMetaProto.TransferMeta> |  |
| METHODID_CHECK_STATUS_NOW = 2 | int |  |
| SERVICE_NAME = "com.welab.wefe.gateway.api.service.proto.TransferService" | String |  |
| getSendMethod | io.grpc.MethodDescriptor<com.welab.wefe.gateway.api.meta.basic.GatewayMetaProto.TransferMeta,
      com.welab.wefe.gateway.api.meta.basic.BasicMetaProto.ReturnStatus> |  |
| serviceDescriptor | io.grpc.ServiceDescriptor |  |
| getRecvMethod | io.grpc.MethodDescriptor<com.welab.wefe.gateway.api.meta.basic.GatewayMetaProto.TransferMeta,
      com.welab.wefe.gateway.api.meta.basic.GatewayMetaProto.TransferMeta> |  |
| METHODID_SEND = 0 | int |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| newStub | TransferServiceStub |  |
| getSendMethod | io.grpc.MethodDescriptor<com.welab.wefe.gateway.api.meta.basic.GatewayMetaProto.TransferMeta,
      com.welab.wefe.gateway.api.meta.basic.BasicMetaProto.ReturnStatus> |  |
| newBlockingStub | TransferServiceBlockingStub |  |
| getRecvMethod | io.grpc.MethodDescriptor<com.welab.wefe.gateway.api.meta.basic.GatewayMetaProto.TransferMeta,
      com.welab.wefe.gateway.api.meta.basic.GatewayMetaProto.TransferMeta> |  |
| newFutureStub | TransferServiceFutureStub |  |
| getCheckStatusNowMethod | io.grpc.MethodDescriptor<com.welab.wefe.gateway.api.meta.basic.GatewayMetaProto.TransferMeta,
      com.welab.wefe.gateway.api.meta.basic.GatewayMetaProto.TransferMeta> |  |
| getServiceDescriptor | io.grpc.ServiceDescriptor |  |




