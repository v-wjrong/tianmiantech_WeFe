# Basic Information

|      |      |
|------|------|
| Name | DataResourceDefaultTag |
| Language | .java |
| Code Path | WeFe/common/java/common-data-mongodb/src/main/java/com/welab/wefe/common/data/mongodb/entity/union/DataResourceDefaultTag.java |
| Package Name | com.welab.wefe.common.data.mongodb.entity.union |
| Dependencies | ['com.welab.wefe.common.data.mongodb.constant.MongodbTable', 'com.welab.wefe.common.data.mongodb.entity.base.AbstractBlockChainBusinessModel', 'com.welab.wefe.common.data.mongodb.entity.union.ext.DataResourceDefaultTagExtJSON', 'com.welab.wefe.common.wefe.enums.DataResourceType', 'org.springframework.data.mongodb.core.mapping.Document', 'java.util.UUID'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| DataResourceDefaultTag | class |  |



## Class DataResourceDefaultTag

|      |      |
|------|------|
| Access Modifier | @Document(collection = MongodbTable.Union.DATA_RESOURCE_DEFAULT_TAG);public |
| Type | class |
| Name | DataResourceDefaultTag |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| tagName | String |  |
| extJson = new DataResourceDefaultTagExtJSON() | DataResourceDefaultTagExtJSON |  |
| tagId = UUID.randomUUID().toString().replaceAll("-", "") | String |  |
| dataResourceType | DataResourceType |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getTagName | String |  |
| getDataResourceType | DataResourceType |  |
| setTagId | void |  |
| setTagName | void |  |
| getTagId | String |  |
| setDataResourceType | void |  |
| getExtJson | DataResourceDefaultTagExtJSON |  |
| setExtJson | void |  |




