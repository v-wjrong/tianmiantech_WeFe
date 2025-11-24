# 基础信息

|      |      |
|------|------|
| 名称 | DataResourceUploadTaskMysqlModel |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/database/entity/data_resource/DataResourceUploadTaskMysqlModel.java |
| 包名 | com.welab.wefe.board.service.database.entity.data_resource |
| 依赖项 | ['com.welab.wefe.board.service.database.entity.base.AbstractBaseMySqlModel', 'com.welab.wefe.common.wefe.enums.DataResourceType', 'com.welab.wefe.common.wefe.enums.DataResourceUploadStatus', 'javax.persistence.Entity', 'javax.persistence.EnumType', 'javax.persistence.Enumerated', 'javax.persistence.Table'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| DataResourceUploadTaskMysqlModel | class |  |



## 类 DataResourceUploadTaskMysqlModel

|      |      |
|------|------|
| 访问范围 | @Entity(name = "data_resource_upload_task");@Table(name = "data_resource_upload_task");public |
| 类型 | class |
| 名称 | DataResourceUploadTaskMysqlModel |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
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

### 方法列表

| 名称  | 类型  | 说明 |
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




