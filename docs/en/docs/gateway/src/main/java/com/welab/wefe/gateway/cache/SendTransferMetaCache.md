# Basic Information

|      |      |
|------|------|
| Name | SendTransferMetaCache |
| Language | .java |
| Code Path | WeFe/gateway/src/main/java/com/welab/wefe/gateway/cache/SendTransferMetaCache.java |
| Package Name | com.welab.wefe.gateway.cache |
| Dependencies | ['com.welab.wefe.gateway.GatewayServer', 'com.welab.wefe.gateway.api.meta.basic.GatewayMetaProto', 'com.welab.wefe.gateway.service.base.AbstractSendTransferMetaCachePersistentService', 'org.apache.commons.collections4.CollectionUtils', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.util.List', 'java.util.concurrent.ConcurrentLinkedQueue'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| SendTransferMetaCache | class |  |



## Class SendTransferMetaCache

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | SendTransferMetaCache |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| sendTransferMetaCache = new SendTransferMetaCache() | SendTransferMetaCache |  |
| dataQueue = new ConcurrentLinkedQueue<>() | ConcurrentLinkedQueue<GatewayMetaProto.TransferMeta> |  |
| LOG = LoggerFactory.getLogger(SendTransferMetaCache.class) | Logger |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getInstance | SendTransferMetaCache |  |
| add | void |  |
| poll | GatewayMetaProto.TransferMeta |  |
| isEmpty | boolean |  |
| refreshCache | boolean |  |




