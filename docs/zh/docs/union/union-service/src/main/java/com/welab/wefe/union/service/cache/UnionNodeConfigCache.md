# 基础信息

|      |      |
|------|------|
| 名称 | UnionNodeConfigCache |
| 编码语言 | .java |
| 代码路径 | WeFe/union/union-service/src/main/java/com/welab/wefe/union/service/cache/UnionNodeConfigCache.java |
| 包名 | com.welab.wefe.union.service.cache |
| 依赖项 | ['com.welab.wefe.common.data.mongodb.entity.base.AbstractUnionNodeConfigMongoModel', 'com.welab.wefe.common.data.mongodb.entity.union.UnionNodeSm2Config', 'com.welab.wefe.union.service.constant.UnionNodeConfigType', 'java.util.concurrent.ConcurrentHashMap'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| UnionNodeConfigCache | class |  |



## 类 UnionNodeConfigCache

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | UnionNodeConfigCache |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| unionNodeConfigMap = new ConcurrentHashMap<>() | ConcurrentHashMap<String, AbstractUnionNodeConfigMongoModel> |  |
| currentBlockchainNodeId | String |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getSm2PrivateKey | String |  |
| setUnionNodeSm2Config | void |  |
| getSm2PublicKey | String |  |




