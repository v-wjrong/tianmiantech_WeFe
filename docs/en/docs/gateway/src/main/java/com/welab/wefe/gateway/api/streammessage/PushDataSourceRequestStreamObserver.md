# Basic Information

|      |      |
|------|------|
| Name | PushDataSourceRequestStreamObserver |
| Language | .java |
| Code Path | WeFe/gateway/src/main/java/com/welab/wefe/gateway/api/streammessage/PushDataSourceRequestStreamObserver.java |
| Package Name | com.welab.wefe.gateway.api.streammessage |
| Dependencies | ['com.welab.wefe.gateway.GatewayServer', 'com.welab.wefe.gateway.api.meta.basic.GatewayMetaProto', 'com.welab.wefe.gateway.service.processors.DsourceProcessor', 'io.grpc.stub.StreamObserver', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| PushDataSourceRequestStreamObserver | class |  |



## Class PushDataSourceRequestStreamObserver

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | PushDataSourceRequestStreamObserver |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| responseObserver | StreamObserver<GatewayMetaProto.TransferMeta> |  |
| LOG = LoggerFactory.getLogger(PushDataSourceRequestStreamObserver.class) | Logger |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| onNext | void |  |
| onError | void |  |
| onCompleted | void |  |




