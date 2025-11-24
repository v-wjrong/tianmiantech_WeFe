# Basic Information

|      |      |
|------|------|
| Name | UnionNodeConfigCache |
| Language | .java |
| Code Path | WeFe/union/union-service/src/main/java/com/welab/wefe/union/service/cache/UnionNodeConfigCache.java |
| Package Name | com.welab.wefe.union.service.cache |
| Dependencies | ['com.welab.wefe.common.data.mongodb.entity.base.AbstractUnionNodeConfigMongoModel', 'com.welab.wefe.common.data.mongodb.entity.union.UnionNodeSm2Config', 'com.welab.wefe.union.service.constant.UnionNodeConfigType', 'java.util.concurrent.ConcurrentHashMap'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| UnionNodeConfigCache | class |  |



## Class UnionNodeConfigCache

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | UnionNodeConfigCache |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| unionNodeConfigMap = new ConcurrentHashMap<>() | ConcurrentHashMap<String, AbstractUnionNodeConfigMongoModel> |  |
| currentBlockchainNodeId | String |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getSm2PrivateKey | String |  |
| setUnionNodeSm2Config | void |  |
| getSm2PublicKey | String |  |




