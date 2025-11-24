# 基础信息

|      |      |
|------|------|
| 名称 | TaskProgressMysqlModel |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/database/entity/job/TaskProgressMysqlModel.java |
| 包名 | com.welab.wefe.board.service.database.entity.job |
| 依赖项 | ['com.welab.wefe.board.service.database.entity.base.AbstractBaseMySqlModel', 'com.welab.wefe.common.wefe.enums.ComponentType', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'javax.persistence.Entity', 'javax.persistence.EnumType', 'javax.persistence.Enumerated', 'java.util.Date'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| TaskProgressMysqlModel | class |  |



## 类 TaskProgressMysqlModel

|      |      |
|------|------|
| 访问范围 | @Entity(name = "task_progress");public |
| 类型 | class |
| 名称 | TaskProgressMysqlModel |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
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

### 方法列表

| 名称  | 类型  | 说明 |
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




