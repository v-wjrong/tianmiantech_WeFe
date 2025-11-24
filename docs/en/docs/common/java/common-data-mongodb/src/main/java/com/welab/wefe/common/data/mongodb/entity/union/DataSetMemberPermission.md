# Basic Information

|      |      |
|------|------|
| Name | DataSetMemberPermission |
| Language | .java |
| Code Path | WeFe/common/java/common-data-mongodb/src/main/java/com/welab/wefe/common/data/mongodb/entity/union/DataSetMemberPermission.java |
| Package Name | com.welab.wefe.common.data.mongodb.entity.union |
| Dependencies | ['com.welab.wefe.common.data.mongodb.constant.MongodbTable', 'com.welab.wefe.common.data.mongodb.entity.base.AbstractBlockChainBusinessModel', 'com.welab.wefe.common.data.mongodb.entity.union.ext.DataSetMemberPermissionExtJSON', 'org.springframework.data.mongodb.core.mapping.Document'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| DataSetMemberPermission | class |  |



## Class DataSetMemberPermission

|      |      |
|------|------|
| Access Modifier | @Document(collection = MongodbTable.Union.DATASET_MEMBER_PERMISSION);public |
| Type | class |
| Name | DataSetMemberPermission |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| extJson = new DataSetMemberPermissionExtJSON() | DataSetMemberPermissionExtJSON |  |
| dataSetMemberPermissionId | String |  |
| memberId | String |  |
| dataSetId | String |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getDataSetMemberPermissionId | String |  |
| setDataSetMemberPermissionId | void |  |
| getMemberId | String |  |
| getDataSetId | String |  |
| setDataSetId | void |  |
| setMemberId | void |  |
| getExtJson | DataSetMemberPermissionExtJSON |  |
| setExtJson | void |  |




