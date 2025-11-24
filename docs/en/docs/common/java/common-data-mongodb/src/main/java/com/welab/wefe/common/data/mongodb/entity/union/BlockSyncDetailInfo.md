# Basic Information

|      |      |
|------|------|
| Name | BlockSyncDetailInfo |
| Language | .java |
| Code Path | WeFe/common/java/common-data-mongodb/src/main/java/com/welab/wefe/common/data/mongodb/entity/union/BlockSyncDetailInfo.java |
| Package Name | com.welab.wefe.common.data.mongodb.entity.union |
| Dependencies | ['com.alibaba.fastjson.JSONObject', 'com.welab.wefe.common.data.mongodb.constant.MongodbTable', 'com.welab.wefe.common.data.mongodb.entity.base.AbstractNormalMongoModel', 'org.springframework.data.mongodb.core.mapping.Document'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| BlockSyncDetailInfo | class |  |



## Class BlockSyncDetailInfo

|      |      |
|------|------|
| Access Modifier | @Document(collection = MongodbTable.Union.BLOCK_SYNC_DETAIL_INFO);public |
| Type | class |
| Name | BlockSyncDetailInfo |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| groupId | Integer |  |
| blockNumber | Long |  |
| data | JSONObject |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getGroupId | Integer |  |
| getBlockNumber | Long |  |
| setBlockNumber | void |  |
| setData | void |  |
| getData | JSONObject |  |
| setGroupId | void |  |




