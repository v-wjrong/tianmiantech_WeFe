# Basic Information

|      |      |
|------|------|
| Name | TaskResultMySqlModel |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/database/entity/job/TaskResultMySqlModel.java |
| Package Name | com.welab.wefe.board.service.database.entity.job |
| Dependencies | ['com.welab.wefe.board.service.database.entity.base.AbstractBaseMySqlModel', 'com.welab.wefe.common.wefe.enums.ComponentType', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'javax.persistence.Entity', 'javax.persistence.EnumType', 'javax.persistence.Enumerated'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| TaskResultMySqlModel | class |  |



## Class TaskResultMySqlModel

|      |      |
|------|------|
| Access Modifier | @Entity(name = "task_result");public |
| Type | class |
| Name | TaskResultMySqlModel |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| flowNodeId | String |  |
| jobId | String |  |
| type | String |  |
| name | String |  |
| componentType | ComponentType |  |
| projectId | String |  |
| taskId | String |  |
| flowId | String |  |
| servingModel | boolean |  |
| result | String |  |
| role | JobMemberRole |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| setRole | void |  |
| setComponentType | void |  |
| setJobId | void |  |
| getName | String |  |
| getComponentType | ComponentType |  |
| getType | String |  |
| getModelId | String |  |
| getTaskId | String |  |
| setTaskId | void |  |
| getFlowId | String |  |
| getRole | JobMemberRole |  |
| getJobId | String |  |
| setFlowId | void |  |
| getFlowNodeId | String |  |
| setFlowNodeId | void |  |
| setName | void |  |
| setType | void |  |
| getResult | String |  |
| setResult | void |  |
| isServingModel | boolean |  |
| setServingModel | void |  |
| getProjectId | String |  |
| setProjectId | void |  |




