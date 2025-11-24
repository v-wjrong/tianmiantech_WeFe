# Basic Information

|      |      |
|------|------|
| Name | PredictStatisticsMySqlModel |
| Language | .java |
| Code Path | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/database/entity/PredictStatisticsMySqlModel.java |
| Package Name | com.welab.wefe.serving.service.database.entity |
| Dependencies | ['com.welab.wefe.common.util.DateUtil', 'javax.persistence', 'java.util.Date'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| PredictStatisticsMySqlModel | class |  |



## Class PredictStatisticsMySqlModel

|      |      |
|------|------|
| Access Modifier | @Entity(name = "predict_statistics");public |
| Type | class |
| Name | PredictStatisticsMySqlModel |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| createdTime = new Date() | Date |  |
| id | int |  |
| fail | long |  |
| minute | String |  |
| hour | String |  |
| day | String |  |
| updatedTime | Date |  |
| total | long |  |
| success | long |  |
| modelId | String |  |
| memberId | String |  |
| month | String |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getMinute | String |  |
| getFail | long |  |
| getTotal | long |  |
| setMonth | void |  |
| setMinute | void |  |
| setHour | void |  |
| getHour | String |  |
| setMemberId | void |  |
| getCreatedTime | Date |  |
| setTotal | void |  |
| getMonth | String |  |
| setId | void |  |
| getId | int |  |
| setSuccess | void |  |
| setCreatedTime | void |  |
| getDay | String |  |
| setModelId | void |  |
| getModelId | String |  |
| setDay | void |  |
| getMemberId | String |  |
| getSuccess | long |  |
| getUpdatedTime | Date |  |
| setFail | void |  |
| setUpdatedTime | void |  |
| setDateFields | void |  |




