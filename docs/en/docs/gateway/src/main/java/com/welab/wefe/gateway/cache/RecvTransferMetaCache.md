# Basic Information

|      |      |
|------|------|
| Name | RecvTransferMetaCache |
| Language | .java |
| Code Path | WeFe/gateway/src/main/java/com/welab/wefe/gateway/cache/RecvTransferMetaCache.java |
| Package Name | com.welab.wefe.gateway.cache |
| Dependencies | ['com.welab.wefe.gateway.GatewayServer', 'com.welab.wefe.gateway.api.meta.basic.GatewayMetaProto', 'com.welab.wefe.gateway.service.base.AbstractRecvTransferMetaCachePersistentService', 'org.apache.commons.collections4.CollectionUtils', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.util.List', 'java.util.concurrent.ConcurrentHashMap'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| RecvTransferMetaCache | class |  |



## Class RecvTransferMetaCache

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | RecvTransferMetaCache |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| dataMap = new ConcurrentHashMap<>() | ConcurrentHashMap<String, GatewayMetaProto.TransferMeta> |  |
| recvTransferMetaCache = new RecvTransferMetaCache() | RecvTransferMetaCache |  |
| LOG = LoggerFactory.getLogger(RecvTransferMetaCache.class) | Logger |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| refreshCache | boolean |  |
| getInstance | RecvTransferMetaCache |  |
| put | void |  |
| get | GatewayMetaProto.TransferMeta |  |
| remove | GatewayMetaProto.TransferMeta |  |




