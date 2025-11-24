# Basic Information

|      |      |
|------|------|
| Name | DataResourceUploadTaskMysqlModel |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/database/entity/data_resource/DataResourceUploadTaskMysqlModel.java |
| Package Name | com.welab.wefe.board.service.database.entity.data_resource |
| Dependencies | ['com.welab.wefe.board.service.database.entity.base.AbstractBaseMySqlModel', 'com.welab.wefe.common.wefe.enums.DataResourceType', 'com.welab.wefe.common.wefe.enums.DataResourceUploadStatus', 'javax.persistence.Entity', 'javax.persistence.EnumType', 'javax.persistence.Enumerated', 'javax.persistence.Table'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| DataResourceUploadTaskMysqlModel | class |  |



## Class DataResourceUploadTaskMysqlModel

|      |      |
|------|------|
| Access Modifier | @Entity(name = "data_resource_upload_task");@Table(name = "data_resource_upload_task");public |
| Type | class |
| Name | DataResourceUploadTaskMysqlModel |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| estimateRemainingTime | long |  |
| dataResourceType | DataResourceType |  |
| dataResourceName | String |  |
| progressRatio | Integer |  |
| completedDataCount | long |  |
| invalidDataCount | long |  |
| errorMessage | String |  |
| dataResourceId | String |  |
| status | DataResourceUploadStatus |  |
| totalDataCount | Long |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getProgressRatio | Integer |  |
| getDataResourceType | DataResourceType |  |
| setCompletedDataCount | void |  |
| getCompletedDataCount | long |  |
| setEstimateRemainingTime | void |  |
| setDataResourceType | void |  |
| getDataResourceId | String |  |
| setDataResourceId | void |  |
| getTotalDataCount | Long |  |
| setTotalDataCount | void |  |
| setDataResourceName | void |  |
| setInvalidDataCount | void |  |
| getDataResourceName | String |  |
| setProgressRatio | void |  |
| getEstimateRemainingTime | long |  |
| getErrorMessage | String |  |
| getInvalidDataCount | long |  |
| setErrorMessage | void |  |
| getStatus | DataResourceUploadStatus |  |
| setStatus | void |  |




