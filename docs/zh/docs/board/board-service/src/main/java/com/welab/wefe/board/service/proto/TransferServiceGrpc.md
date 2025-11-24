# 基础信息

|      |      |
|------|------|
| 名称 | TransferServiceGrpc |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/proto/TransferServiceGrpc.java |
| 包名 | com.welab.wefe.board.service.proto |
| 依赖项 | ['com.welab.wefe.board.service.proto.meta.basic.BasicMetaProto', 'com.welab.wefe.board.service.proto.meta.basic.GatewayMetaProto', 'io.grpc.MethodDescriptor.generateFullMethodName', 'io.grpc.stub.ClientCalls.asyncUnaryCall', 'io.grpc.stub.ClientCalls.blockingUnaryCall', 'io.grpc.stub.ClientCalls.futureUnaryCall', 'io.grpc.stub.ServerCalls.asyncUnaryCall', 'io.grpc.stub.ServerCalls.asyncUnimplementedUnaryCall'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| TransferServiceGrpc | class |  |



## 类 TransferServiceGrpc

|      |      |
|------|------|
| 访问范围 | @javax.annotation.Generated(;    value = "by gRPC proto compiler (version 1.29.0)",;    comments = "Source: gateway-service.proto");public final |
| 类型 | class |
| 名称 | TransferServiceGrpc |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
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

### 方法列表

| 名称  | 类型  | 说明 |
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




