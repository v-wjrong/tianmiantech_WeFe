# Basic Information

|      |      |
|------|------|
| Name | DataResourceLazyUpdateModel |
| Language | .java |
| Code Path | WeFe/common/java/common-data-mongodb/src/main/java/com/welab/wefe/common/data/mongodb/entity/union/DataResourceLazyUpdateModel.java |
| Package Name | com.welab.wefe.common.data.mongodb.entity.union |
| Dependencies | ['com.welab.wefe.common.data.mongodb.constant.MongodbTable', 'com.welab.wefe.common.data.mongodb.entity.base.AbstractNormalMongoModel', 'com.welab.wefe.common.wefe.enums.DataResourceType', 'org.springframework.data.mongodb.core.mapping.Document'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| DataResourceLazyUpdateModel | class |  |



## Class DataResourceLazyUpdateModel

|      |      |
|------|------|
| Access Modifier | @Document(collection = MongodbTable.Union.DATA_RESOURCE_LAZY_UPDATE_MODEL);public |
| Type | class |
| Name | DataResourceLazyUpdateModel |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| usageCountInMember | int |  |
| labeledCount | int |  |
| dataResourceId | String |  |
| labelCompleted | boolean |  |
| usageCountInJob | int |  |
| labelList | String |  |
| usageCountInFlow | int |  |
| totalDataCount | int |  |
| usageCountInProject | int |  |
| dataResourceType | DataResourceType |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getUsageCountInFlow | int |  |
| setUsageCountInProject | void |  |
| setUsageCountInMember | void |  |
| setTotalDataCount | void |  |
| getUsageCountInJob | int |  |
| isLabelCompleted | boolean |  |
| setUsageCountInFlow | void |  |
| getTotalDataCount | int |  |
| getLabeledCount | int |  |
| setLabelList | void |  |
| setDataResourceId | void |  |
| getLabelList | String |  |
| setLabeledCount | void |  |
| getUsageCountInProject | int |  |
| getUsageCountInMember | int |  |
| getDataResourceId | String |  |
| setUsageCountInJob | void |  |
| setLabelCompleted | void |  |
| getDataResourceType | DataResourceType |  |
| setDataResourceType | void |  |




