# Basic Information

|      |      |
|------|------|
| Name | ImageDataSetMysqlModel |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/database/entity/data_resource/ImageDataSetMysqlModel.java |
| Package Name | com.welab.wefe.board.service.database.entity.data_resource |
| Dependencies | ['com.alibaba.fastjson.annotation.JSONField', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.wefe.enums.DataResourceType', 'com.welab.wefe.common.wefe.enums.DeepLearningJobType', 'javax.persistence.Entity', 'javax.persistence.EnumType', 'javax.persistence.Enumerated', 'javax.persistence.Table', 'java.util.List', 'java.util.TreeSet'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| ImageDataSetMysqlModel | class |  |



## Class ImageDataSetMysqlModel

|      |      |
|------|------|
| Access Modifier | @Entity(name = "image_data_set");@Table(name = "image_data_set");public |
| Type | class |
| Name | ImageDataSetMysqlModel |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| labelCompleted | boolean |  |
| labeledCount | Long |  |
| forJobType | DeepLearningJobType |  |
| labelList | String |  |
| filesSize | Long |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| isLabelCompleted | boolean |  |
| setLabelCompleted | void |  |
| getLabelSet | TreeSet<String> |  |
| getForJobType | DeepLearningJobType |  |
| setForJobType | void |  |
| setLabeledCount | void |  |
| getLabeledCount | Long |  |
| setLabelList | void |  |
| getLabelList | String |  |
| getFilesSize | Long |  |
| setFilesSize | void |  |




