# 基础信息

|      |      |
|------|------|
| 名称 | PushDataSourceRequestStreamObserver |
| 编码语言 | .java |
| 代码路径 | WeFe/gateway/src/main/java/com/welab/wefe/gateway/api/streammessage/PushDataSourceRequestStreamObserver.java |
| 包名 | com.welab.wefe.gateway.api.streammessage |
| 依赖项 | ['com.welab.wefe.gateway.GatewayServer', 'com.welab.wefe.gateway.api.meta.basic.GatewayMetaProto', 'com.welab.wefe.gateway.service.processors.DsourceProcessor', 'io.grpc.stub.StreamObserver', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| PushDataSourceRequestStreamObserver | class |  |



## 类 PushDataSourceRequestStreamObserver

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | PushDataSourceRequestStreamObserver |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| responseObserver | StreamObserver<GatewayMetaProto.TransferMeta> |  |
| LOG = LoggerFactory.getLogger(PushDataSourceRequestStreamObserver.class) | Logger |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| onNext | void |  |
| onError | void |  |
| onCompleted | void |  |




