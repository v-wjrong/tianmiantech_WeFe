# Basic Information

|      |      |
|------|------|
| Name | TaskMySqlModel |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/database/entity/job/TaskMySqlModel.java |
| Package Name | com.welab.wefe.board.service.database.entity.job |
| Dependencies | ['com.welab.wefe.board.service.database.entity.base.AbstractBaseMySqlModel', 'com.welab.wefe.common.wefe.enums.ComponentType', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'com.welab.wefe.common.wefe.enums.TaskStatus', 'javax.persistence.Entity', 'javax.persistence.EnumType', 'javax.persistence.Enumerated', 'java.util.Date'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| TaskMySqlModel | class |  |



## Class TaskMySqlModel

|      |      |
|------|------|
| Access Modifier | @Entity(name = "task");public |
| Type | class |
| Name | TaskMySqlModel |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| role | JobMemberRole |  |
| flowId | String |  |
| flowNodeId | String |  |
| deep | Integer |  |
| name | String |  |
| finishTime | Date |  |
| status | TaskStatus |  |
| errorCause | String |  |
| jobId | String |  |
| position | Integer |  |
| message | String |  |
| parentTaskIdList | String |  |
| taskId | String |  |
| taskConf | String |  |
| taskType | ComponentType |  |
| spend | Integer |  |
| projectId | String |  |
| startTime | Date |  |
| dependenceList | String |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getPosition | Integer |  |
| setDeep | void |  |
| getStartTime | Date |  |
| setParentTaskIdList | void |  |
| setMessage | void |  |
| getDependenceList | String |  |
| getFlowId | String |  |
| getTaskConf | String |  |
| getParentTaskIdList | String |  |
| setRole | void |  |
| setTaskConf | void |  |
| setFlowNodeId | void |  |
| getFlowNodeId | String |  |
| getStatus | TaskStatus |  |
| getTaskId | String |  |
| setTaskType | void |  |
| getSpend | Integer |  |
| getDeep | Integer |  |
| getFinishTime | Date |  |
| setStartTime | void |  |
| setErrorCause | void |  |
| setTaskId | void |  |
| getTaskType | ComponentType |  |
| getJobId | String |  |
| getRole | JobMemberRole |  |
| setName | void |  |
| setSpend | void |  |
| getName | String |  |
| getErrorCause | String |  |
| setStatus | void |  |
| setJobId | void |  |
| setDependenceList | void |  |
| setFinishTime | void |  |
| getMessage | String |  |
| setFlowId | void |  |
| setPosition | void |  |
| getProjectId | String |  |
| setProjectId | void |  |




