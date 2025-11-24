# 基础信息

|      |      |
|------|------|
| 名称 | TaskResultMySqlModel |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/database/entity/job/TaskResultMySqlModel.java |
| 包名 | com.welab.wefe.board.service.database.entity.job |
| 依赖项 | ['com.welab.wefe.board.service.database.entity.base.AbstractBaseMySqlModel', 'com.welab.wefe.common.wefe.enums.ComponentType', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'javax.persistence.Entity', 'javax.persistence.EnumType', 'javax.persistence.Enumerated'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| TaskResultMySqlModel | class |  |



## 类 TaskResultMySqlModel

|      |      |
|------|------|
| 访问范围 | @Entity(name = "task_result");public |
| 类型 | class |
| 名称 | TaskResultMySqlModel |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
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

### 方法列表

| 名称  | 类型  | 说明 |
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




