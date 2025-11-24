# 基础信息

|      |      |
|------|------|
| 名称 | TransferServiceGrpc |
| 编码语言 | .java |
| 代码路径 | WeFe/gateway/src/main/java/com/welab/wefe/gateway/api/service/proto/TransferServiceGrpc.java |
| 包名 | com.welab.wefe.gateway.api.service.proto |
| 依赖项 | ['io.grpc.MethodDescriptor.generateFullMethodName', 'io.grpc.stub.ClientCalls.asyncUnaryCall', 'io.grpc.stub.ClientCalls.blockingUnaryCall', 'io.grpc.stub.ClientCalls.futureUnaryCall', 'io.grpc.stub.ServerCalls.asyncUnaryCall', 'io.grpc.stub.ServerCalls.asyncUnimplementedUnaryCall'] |
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

### 方法列表

| 名称  | 类型  | 说明 |
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




