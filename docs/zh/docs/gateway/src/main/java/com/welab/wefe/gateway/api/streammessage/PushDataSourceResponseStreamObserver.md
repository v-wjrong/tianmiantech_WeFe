# 基础信息

|      |      |
|------|------|
| 名称 | PushDataSourceResponseStreamObserver |
| 编码语言 | .java |
| 代码路径 | WeFe/gateway/src/main/java/com/welab/wefe/gateway/api/streammessage/PushDataSourceResponseStreamObserver.java |
| 包名 | com.welab.wefe.gateway.api.streammessage |
| 依赖项 | ['com.google.common.util.concurrent.SettableFuture', 'com.welab.wefe.gateway.api.meta.basic.GatewayMetaProto', 'com.welab.wefe.gateway.service.base.AbstractTransferMetaDataSource', 'io.grpc.stub.StreamObserver', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| PushDataSourceResponseStreamObserver | class |  |



## 类 PushDataSourceResponseStreamObserver

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | PushDataSourceResponseStreamObserver |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| asyncResponseCollector | AbstractTransferMetaDataSource.AsyncResponseCollector |  |
| LOG = LoggerFactory.getLogger(PushDataSourceResponseStreamObserver.class) | Logger |  |
| finishFuture | SettableFuture<Void> |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| onNext | void |  |
| onError | void |  |
| onCompleted | void |  |




