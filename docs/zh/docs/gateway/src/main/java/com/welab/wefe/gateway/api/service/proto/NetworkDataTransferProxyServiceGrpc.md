# 基础信息

|      |      |
|------|------|
| 名称 | NetworkDataTransferProxyServiceGrpc |
| 编码语言 | .java |
| 代码路径 | WeFe/gateway/src/main/java/com/welab/wefe/gateway/api/service/proto/NetworkDataTransferProxyServiceGrpc.java |
| 包名 | com.welab.wefe.gateway.api.service.proto |
| 依赖项 | ['io.grpc.MethodDescriptor.generateFullMethodName', 'io.grpc.stub.ClientCalls.asyncBidiStreamingCall', 'io.grpc.stub.ClientCalls.asyncUnaryCall', 'io.grpc.stub.ClientCalls', 'io.grpc.stub.ServerCalls.asyncBidiStreamingCall', 'io.grpc.stub.ServerCalls.asyncUnaryCall', 'io.grpc.stub.ServerCalls'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| NetworkDataTransferProxyServiceGrpc | class |  |



## 类 NetworkDataTransferProxyServiceGrpc

|      |      |
|------|------|
| 访问范围 | @javax.annotation.Generated(;    value = "by gRPC proto compiler (version 1.29.0)",;    comments = "Source: gateway-service.proto");public final |
| 类型 | class |
| 名称 | NetworkDataTransferProxyServiceGrpc |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| METHODID_PUSH = 0 | int |  |
| SERVICE_NAME = "com.welab.wefe.gateway.api.service.proto.NetworkDataTransferProxyService" | String |  |
| serviceDescriptor | io.grpc.ServiceDescriptor |  |
| getPushMethod | io.grpc.MethodDescriptor<com.welab.wefe.gateway.api.meta.basic.GatewayMetaProto.TransferMeta,
      com.welab.wefe.gateway.api.meta.basic.BasicMetaProto.ReturnStatus> |  |
| METHODID_PUSH_DATA_SOURCE = 1 | int |  |
| getPushDataSourceMethod | io.grpc.MethodDescriptor<com.welab.wefe.gateway.api.meta.basic.GatewayMetaProto.TransferMeta,
      com.welab.wefe.gateway.api.meta.basic.GatewayMetaProto.TransferMeta> |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getPushMethod | io.grpc.MethodDescriptor<com.welab.wefe.gateway.api.meta.basic.GatewayMetaProto.TransferMeta,
      com.welab.wefe.gateway.api.meta.basic.BasicMetaProto.ReturnStatus> |  |
| newStub | NetworkDataTransferProxyServiceStub |  |
| getPushDataSourceMethod | io.grpc.MethodDescriptor<com.welab.wefe.gateway.api.meta.basic.GatewayMetaProto.TransferMeta,
      com.welab.wefe.gateway.api.meta.basic.GatewayMetaProto.TransferMeta> |  |
| newBlockingStub | NetworkDataTransferProxyServiceBlockingStub |  |
| newFutureStub | NetworkDataTransferProxyServiceFutureStub |  |
| getServiceDescriptor | io.grpc.ServiceDescriptor |  |




