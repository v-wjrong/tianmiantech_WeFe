# 基础信息

|      |      |
|------|------|
| 名称 | TaskOutputModel |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/dto/entity/job/TaskOutputModel.java |
| 包名 | com.welab.wefe.board.service.dto.entity.job |
| 依赖项 | ['com.alibaba.fastjson.JSON', 'com.alibaba.fastjson.JSONObject', 'com.welab.wefe.board.service.dto.entity.AbstractOutputModel', 'com.welab.wefe.common.fieldvalidate.annotation.Check', 'com.welab.wefe.common.wefe.enums.ComponentType', 'com.welab.wefe.common.wefe.enums.TaskStatus', 'java.util.Date'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| TaskOutputModel | class |  |



## 类 TaskOutputModel

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | TaskOutputModel |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
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

### 方法列表

| 名称  | 类型  | 说明 |
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




