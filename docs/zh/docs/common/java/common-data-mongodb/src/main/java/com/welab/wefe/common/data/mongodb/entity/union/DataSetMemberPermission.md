# 基础信息

|      |      |
|------|------|
| 名称 | DataSetMemberPermission |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-data-mongodb/src/main/java/com/welab/wefe/common/data/mongodb/entity/union/DataSetMemberPermission.java |
| 包名 | com.welab.wefe.common.data.mongodb.entity.union |
| 依赖项 | ['com.welab.wefe.common.data.mongodb.constant.MongodbTable', 'com.welab.wefe.common.data.mongodb.entity.base.AbstractBlockChainBusinessModel', 'com.welab.wefe.common.data.mongodb.entity.union.ext.DataSetMemberPermissionExtJSON', 'org.springframework.data.mongodb.core.mapping.Document'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| DataSetMemberPermission | class |  |



## 类 DataSetMemberPermission

|      |      |
|------|------|
| 访问范围 | @Document(collection = MongodbTable.Union.DATASET_MEMBER_PERMISSION);public |
| 类型 | class |
| 名称 | DataSetMemberPermission |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| extJson = new DataSetMemberPermissionExtJSON() | DataSetMemberPermissionExtJSON |  |
| dataSetMemberPermissionId | String |  |
| memberId | String |  |
| dataSetId | String |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getDataSetMemberPermissionId | String |  |
| setDataSetMemberPermissionId | void |  |
| getMemberId | String |  |
| getDataSetId | String |  |
| setDataSetId | void |  |
| setMemberId | void |  |
| getExtJson | DataSetMemberPermissionExtJSON |  |
| setExtJson | void |  |




