# 基础信息

|      |      |
|------|------|
| 名称 | TaskMySqlModel |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/database/entity/job/TaskMySqlModel.java |
| 包名 | com.welab.wefe.board.service.database.entity.job |
| 依赖项 | ['com.welab.wefe.board.service.database.entity.base.AbstractBaseMySqlModel', 'com.welab.wefe.common.wefe.enums.ComponentType', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'com.welab.wefe.common.wefe.enums.TaskStatus', 'javax.persistence.Entity', 'javax.persistence.EnumType', 'javax.persistence.Enumerated', 'java.util.Date'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| TaskMySqlModel | class |  |



## 类 TaskMySqlModel

|      |      |
|------|------|
| 访问范围 | @Entity(name = "task");public |
| 类型 | class |
| 名称 | TaskMySqlModel |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
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

### 方法列表

| 名称  | 类型  | 说明 |
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




