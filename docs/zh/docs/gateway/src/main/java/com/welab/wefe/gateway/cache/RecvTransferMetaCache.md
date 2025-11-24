# 基础信息

|      |      |
|------|------|
| 名称 | RecvTransferMetaCache |
| 编码语言 | .java |
| 代码路径 | WeFe/gateway/src/main/java/com/welab/wefe/gateway/cache/RecvTransferMetaCache.java |
| 包名 | com.welab.wefe.gateway.cache |
| 依赖项 | ['com.welab.wefe.gateway.GatewayServer', 'com.welab.wefe.gateway.api.meta.basic.GatewayMetaProto', 'com.welab.wefe.gateway.service.base.AbstractRecvTransferMetaCachePersistentService', 'org.apache.commons.collections4.CollectionUtils', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.util.List', 'java.util.concurrent.ConcurrentHashMap'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| RecvTransferMetaCache | class |  |



## 类 RecvTransferMetaCache

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | RecvTransferMetaCache |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| dataMap = new ConcurrentHashMap<>() | ConcurrentHashMap<String, GatewayMetaProto.TransferMeta> |  |
| recvTransferMetaCache = new RecvTransferMetaCache() | RecvTransferMetaCache |  |
| LOG = LoggerFactory.getLogger(RecvTransferMetaCache.class) | Logger |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| refreshCache | boolean |  |
| getInstance | RecvTransferMetaCache |  |
| put | void |  |
| get | GatewayMetaProto.TransferMeta |  |
| remove | GatewayMetaProto.TransferMeta |  |




