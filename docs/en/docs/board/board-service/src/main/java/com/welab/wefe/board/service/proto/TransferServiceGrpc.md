# Basic Information

|      |      |
|------|------|
| Name | TransferServiceGrpc |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/proto/TransferServiceGrpc.java |
| Package Name | com.welab.wefe.board.service.proto |
| Dependencies | ['com.welab.wefe.board.service.proto.meta.basic.BasicMetaProto', 'com.welab.wefe.board.service.proto.meta.basic.GatewayMetaProto', 'io.grpc.MethodDescriptor.generateFullMethodName', 'io.grpc.stub.ClientCalls.asyncUnaryCall', 'io.grpc.stub.ClientCalls.blockingUnaryCall', 'io.grpc.stub.ClientCalls.futureUnaryCall', 'io.grpc.stub.ServerCalls.asyncUnaryCall', 'io.grpc.stub.ServerCalls.asyncUnimplementedUnaryCall'] |
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
| getCheckStatusNowMethod | io.grpc.MethodDescriptor<GatewayMetaProto.TransferMeta,
      GatewayMetaProto.TransferMeta> |  |
| serviceDescriptor | io.grpc.ServiceDescriptor |  |
| SERVICE_NAME = "com.welab.wefe.gateway.api.service.proto.TransferService" | String |  |
| METHODID_SEND = 0 | int |  |
| getRecvMethod | io.grpc.MethodDescriptor<GatewayMetaProto.TransferMeta,
      GatewayMetaProto.TransferMeta> |  |
| getSendMethod | io.grpc.MethodDescriptor<GatewayMetaProto.TransferMeta,
      BasicMetaProto.ReturnStatus> |  |
| METHODID_CHECK_STATUS_NOW = 2 | int |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| newStub | TransferServiceStub |  |
| getCheckStatusNowMethod | io.grpc.MethodDescriptor<GatewayMetaProto.TransferMeta,
      GatewayMetaProto.TransferMeta> |  |
| getSendMethod | io.grpc.MethodDescriptor<GatewayMetaProto.TransferMeta,
      BasicMetaProto.ReturnStatus> |  |
| newBlockingStub | TransferServiceBlockingStub |  |
| newFutureStub | TransferServiceFutureStub |  |
| getRecvMethod | io.grpc.MethodDescriptor<GatewayMetaProto.TransferMeta,
      GatewayMetaProto.TransferMeta> |  |
| getServiceDescriptor | io.grpc.ServiceDescriptor |  |




