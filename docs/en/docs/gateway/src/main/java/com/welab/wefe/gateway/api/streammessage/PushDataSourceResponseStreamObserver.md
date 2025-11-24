# Basic Information

|      |      |
|------|------|
| Name | PushDataSourceResponseStreamObserver |
| Language | .java |
| Code Path | WeFe/gateway/src/main/java/com/welab/wefe/gateway/api/streammessage/PushDataSourceResponseStreamObserver.java |
| Package Name | com.welab.wefe.gateway.api.streammessage |
| Dependencies | ['com.google.common.util.concurrent.SettableFuture', 'com.welab.wefe.gateway.api.meta.basic.GatewayMetaProto', 'com.welab.wefe.gateway.service.base.AbstractTransferMetaDataSource', 'io.grpc.stub.StreamObserver', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| PushDataSourceResponseStreamObserver | class |  |



## Class PushDataSourceResponseStreamObserver

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | PushDataSourceResponseStreamObserver |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| asyncResponseCollector | AbstractTransferMetaDataSource.AsyncResponseCollector |  |
| LOG = LoggerFactory.getLogger(PushDataSourceResponseStreamObserver.class) | Logger |  |
| finishFuture | SettableFuture<Void> |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| onNext | void |  |
| onError | void |  |
| onCompleted | void |  |




