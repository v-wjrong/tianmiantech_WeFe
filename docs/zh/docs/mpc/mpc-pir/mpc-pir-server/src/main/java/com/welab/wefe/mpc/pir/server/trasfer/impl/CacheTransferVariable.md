# 基础信息

|      |      |
|------|------|
| 名称 | CacheTransferVariable |
| 编码语言 | .java |
| 代码路径 | WeFe/mpc/mpc-pir/mpc-pir-server/src/main/java/com/welab/wefe/mpc/pir/server/trasfer/impl/CacheTransferVariable.java |
| 包名 | com.welab.wefe.mpc.pir.server.trasfer.impl |
| 依赖项 | ['com.welab.wefe.mpc.cache.intermediate.CacheOperation', 'com.welab.wefe.mpc.cache.intermediate.CacheOperationFactory', 'com.welab.wefe.mpc.commom.Constants', 'com.welab.wefe.mpc.pir.server.trasfer.PrivateInformationRetrievalTransferVariable', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.util.concurrent.TimeUnit'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| CacheTransferVariable | class |  |



## 类 CacheTransferVariable

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | CacheTransferVariable |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| mCacheOperation = CacheOperationFactory.getCacheOperation() | CacheOperation<String> |  |
| LOG = LoggerFactory.getLogger(CacheTransferVariable.class) | Logger |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| processHauckRandomLegal | boolean |  |
| processHauckRandom | void |  |
| processResult | void |  |
| processClientRandom | String |  |
| getValue | String |  |




