# Basic Information

|      |      |
|------|------|
| Name | DataSetDefaultTag |
| Language | .java |
| Code Path | WeFe/common/java/common-data-mongodb/src/main/java/com/welab/wefe/common/data/mongodb/entity/union/DataSetDefaultTag.java |
| Package Name | com.welab.wefe.common.data.mongodb.entity.union |
| Dependencies | ['com.welab.wefe.common.data.mongodb.constant.MongodbTable', 'com.welab.wefe.common.data.mongodb.entity.base.AbstractBlockChainBusinessModel', 'com.welab.wefe.common.data.mongodb.entity.union.ext.DataSetDefaultTagExtJSON', 'org.springframework.data.mongodb.core.mapping.Document', 'java.util.UUID'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| DataSetDefaultTag | class |  |



## Class DataSetDefaultTag

|      |      |
|------|------|
| Access Modifier | @Document(collection = MongodbTable.Union.DATA_SET_DEFAULT_TAG);public |
| Type | class |
| Name | DataSetDefaultTag |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| tagName | String |  |
| extJson = new DataSetDefaultTagExtJSON() | DataSetDefaultTagExtJSON |  |
| tagId = UUID.randomUUID().toString().replaceAll("-", "") | String |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getExtJson | DataSetDefaultTagExtJSON |  |
| setTagId | void |  |
| setExtJson | void |  |
| getTagName | String |  |
| setTagName | void |  |
| getTagId | String |  |




