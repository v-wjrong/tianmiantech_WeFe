# Basic Information

|      |      |
|------|------|
| Name | TaskProgressMysqlModel |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/database/entity/job/TaskProgressMysqlModel.java |
| Package Name | com.welab.wefe.board.service.database.entity.job |
| Dependencies | ['com.welab.wefe.board.service.database.entity.base.AbstractBaseMySqlModel', 'com.welab.wefe.common.wefe.enums.ComponentType', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'javax.persistence.Entity', 'javax.persistence.EnumType', 'javax.persistence.Enumerated', 'java.util.Date'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| TaskProgressMysqlModel | class |  |



## Class TaskProgressMysqlModel

|      |      |
|------|------|
| Access Modifier | @Entity(name = "task_progress");public |
| Type | class |
| Name | TaskProgressMysqlModel |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| projectId | String |  |
| progressRate | Double |  |
| progress | Integer |  |
| expectWorkAmount | Integer |  |
| spend | Integer |  |
| reallyWorkAmount | Integer |  |
| expectEndTime | Date |  |
| taskType | ComponentType |  |
| flowNodeId | String |  |
| taskId | String |  |
| role | JobMemberRole |  |
| flowId | String |  |
| jobId | String |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getProgress | Integer |  |
| getTaskType | ComponentType |  |
| getFlowNodeId | String |  |
| setProjectId | void |  |
| getProjectId | String |  |
| setTaskType | void |  |
| setFlowId | void |  |
| getProgressRate | Double |  |
| setProgressRate | void |  |
| getTaskId | String |  |
| setTaskId | void |  |
| setFlowNodeId | void |  |
| setProgress | void |  |
| setReallyWorkAmount | void |  |
| getRole | JobMemberRole |  |
| setJobId | void |  |
| getFlowId | String |  |
| getExpectWorkAmount | Integer |  |
| getJobId | String |  |
| getReallyWorkAmount | Integer |  |
| getSpend | Integer |  |
| setSpend | void |  |
| getExpectEndTime | Date |  |
| setExpectWorkAmount | void |  |
| setRole | void |  |
| setExpectEndTime | void |  |




