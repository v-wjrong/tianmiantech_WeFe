# Basic Information

|      |      |
|------|------|
| Name | ImageDataSet |
| Language | .java |
| Code Path | WeFe/common/java/common-data-mongodb/src/main/java/com/welab/wefe/common/data/mongodb/entity/union/ImageDataSet.java |
| Package Name | com.welab.wefe.common.data.mongodb.entity.union |
| Dependencies | ['com.welab.wefe.common.data.mongodb.constant.MongodbTable', 'com.welab.wefe.common.data.mongodb.entity.base.AbstractBlockChainBusinessModel', 'com.welab.wefe.common.data.mongodb.entity.union.ext.ImageDataSetExtJSON', 'com.welab.wefe.common.wefe.enums.DeepLearningJobType', 'org.springframework.data.mongodb.core.mapping.Document'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| ImageDataSet | class |  |



## Class ImageDataSet

|      |      |
|------|------|
| Access Modifier | @Document(collection = MongodbTable.Union.IMAGE_DATASET);public |
| Type | class |
| Name | ImageDataSet |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| extJson | ImageDataSetExtJSON |  |
| forJobType | DeepLearningJobType |  |
| dataResourceId | String |  |
| labelCompleted | String |  |
| labelList | String |  |
| labeledCount | String |  |
| fileSize | String |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getForJobType | DeepLearningJobType |  |
| getFileSize | String |  |
| getLabeledCount | String |  |
| getLabelList | String |  |
| getExtJson | ImageDataSetExtJSON |  |
| setLabelList | void |  |
| getDataResourceId | String |  |
| setForJobType | void |  |
| setFileSize | void |  |
| setLabelCompleted | void |  |
| setDataResourceId | void |  |
| getLabelCompleted | String |  |
| setLabeledCount | void |  |
| setExtJson | void |  |




