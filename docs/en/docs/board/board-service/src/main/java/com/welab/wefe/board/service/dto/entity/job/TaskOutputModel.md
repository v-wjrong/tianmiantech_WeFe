# Basic Information

|      |      |
|------|------|
| Name | TaskOutputModel |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/dto/entity/job/TaskOutputModel.java |
| Package Name | com.welab.wefe.board.service.dto.entity.job |
| Dependencies | ['com.alibaba.fastjson.JSON', 'com.alibaba.fastjson.JSONObject', 'com.welab.wefe.board.service.dto.entity.AbstractOutputModel', 'com.welab.wefe.common.fieldvalidate.annotation.Check', 'com.welab.wefe.common.wefe.enums.ComponentType', 'com.welab.wefe.common.wefe.enums.TaskStatus', 'java.util.Date'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| TaskOutputModel | class |  |



## Class TaskOutputModel

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | TaskOutputModel |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| finishTime | Date |  |
| position | Integer |  |
| taskConf | JSONObject |  |
| errorCause | String |  |
| status | TaskStatus |  |
| parentTaskIdList | String |  |
| taskType | ComponentType |  |
| dependenceList | String |  |
| name | String |  |
| spend | Integer |  |
| jobId | String |  |
| taskId | String |  |
| flowId | String |  |
| flowNodeId | String |  |
| message | String |  |
| startTime | Date |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getStartTime | Date |  |
| getFinishTime | Date |  |
| setDependenceList | void |  |
| getComponentName | String |  |
| getErrorCause | String |  |
| getFlowNodeId | String |  |
| setFinishTime | void |  |
| getTaskConf | JSONObject |  |
| setTaskId | void |  |
| setStartTime | void |  |
| getMessage | String |  |
| setTaskType | void |  |
| setFlowNodeId | void |  |
| getDependenceList | String |  |
| getJobId | String |  |
| setMessage | void |  |
| getFlowId | String |  |
| setParentTaskIdList | void |  |
| getStatus | TaskStatus |  |
| getName | String |  |
| setStatus | void |  |
| getTaskType | ComponentType |  |
| setJobId | void |  |
| setTaskConf | void |  |
| getTaskId | String |  |
| setName | void |  |
| setFlowId | void |  |
| getParentTaskIdList | String |  |
| setErrorCause | void |  |
| getPosition | Integer |  |
| setPosition | void |  |
| getSpend | Integer |  |
| setSpend | void |  |




