# 基础信息

|      |      |
|------|------|
| 名称 | BlockSyncDetailInfo |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-data-mongodb/src/main/java/com/welab/wefe/common/data/mongodb/entity/union/BlockSyncDetailInfo.java |
| 包名 | com.welab.wefe.common.data.mongodb.entity.union |
| 依赖项 | ['com.alibaba.fastjson.JSONObject', 'com.welab.wefe.common.data.mongodb.constant.MongodbTable', 'com.welab.wefe.common.data.mongodb.entity.base.AbstractNormalMongoModel', 'org.springframework.data.mongodb.core.mapping.Document'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| BlockSyncDetailInfo | class |  |



## 类 BlockSyncDetailInfo

|      |      |
|------|------|
| 访问范围 | @Document(collection = MongodbTable.Union.BLOCK_SYNC_DETAIL_INFO);public |
| 类型 | class |
| 名称 | BlockSyncDetailInfo |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| groupId | Integer |  |
| blockNumber | Long |  |
| data | JSONObject |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getGroupId | Integer |  |
| getBlockNumber | Long |  |
| setBlockNumber | void |  |
| setData | void |  |
| getData | JSONObject |  |
| setGroupId | void |  |




