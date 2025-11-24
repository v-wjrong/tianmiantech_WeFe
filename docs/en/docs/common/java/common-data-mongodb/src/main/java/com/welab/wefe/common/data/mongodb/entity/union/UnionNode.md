# Basic Information

|      |      |
|------|------|
| Name | UnionNode |
| Language | .java |
| Code Path | WeFe/common/java/common-data-mongodb/src/main/java/com/welab/wefe/common/data/mongodb/entity/union/UnionNode.java |
| Package Name | com.welab.wefe.common.data.mongodb.entity.union |
| Dependencies | ['com.welab.wefe.common.data.mongodb.constant.MongodbTable', 'com.welab.wefe.common.data.mongodb.entity.base.AbstractBlockChainBusinessModel', 'com.welab.wefe.common.data.mongodb.entity.union.ext.UnionNodeExtJSON', 'org.springframework.data.mongodb.core.mapping.Document'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| UnionNode | class |  |



## Class UnionNode

|      |      |
|------|------|
| Access Modifier | @Document(collection = MongodbTable.Union.UNION_NODE);public |
| Type | class |
| Name | UnionNode |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
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

### Method List

| Name  | Type  | Description |
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




