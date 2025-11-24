# 基础信息

|      |      |
|------|------|
| 名称 | UnionNode |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-data-mongodb/src/main/java/com/welab/wefe/common/data/mongodb/entity/union/UnionNode.java |
| 包名 | com.welab.wefe.common.data.mongodb.entity.union |
| 依赖项 | ['com.welab.wefe.common.data.mongodb.constant.MongodbTable', 'com.welab.wefe.common.data.mongodb.entity.base.AbstractBlockChainBusinessModel', 'com.welab.wefe.common.data.mongodb.entity.union.ext.UnionNodeExtJSON', 'org.springframework.data.mongodb.core.mapping.Document'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| UnionNode | class |  |



## 类 UnionNode

|      |      |
|------|------|
| 访问范围 | @Document(collection = MongodbTable.Union.UNION_NODE);public |
| 类型 | class |
| 名称 | UnionNode |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| baseUrl | String |  |
| contactEmail | String |  |
| lostContact | String |  |
| blockchainNodeId | String |  |
| nodeId | String |  |
| enable | String |  |
| organizationName | String |  |
| version | String |  |
| priorityLevel | String |  |
| publicKey | String |  |
| extJson = new UnionNodeExtJSON() | UnionNodeExtJSON |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| setOrganizationName | void |  |
| getContactEmail | String |  |
| getOrganizationName | String |  |
| setPriorityLevel | void |  |
| getEnable | String |  |
| setEnable | void |  |
| getExtJson | UnionNodeExtJSON |  |
| setExtJson | void |  |
| getPublicKey | String |  |
| setPublicKey | void |  |
| getBlockchainNodeId | String |  |
| getLostContact | String |  |
| getBaseUrl | String |  |
| setContactEmail | void |  |
| setLostContact | void |  |
| getNodeId | String |  |
| getPriorityLevel | String |  |
| setNodeId | void |  |
| setVersion | void |  |
| setBaseUrl | void |  |
| setBlockchainNodeId | void |  |
| getVersion | String |  |




