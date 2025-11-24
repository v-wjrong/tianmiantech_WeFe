# 基础信息

|      |      |
|------|------|
| 名称 | TaskResultOutputModel |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/dto/entity/job/TaskResultOutputModel.java |
| 包名 | com.welab.wefe.board.service.dto.entity.job |
| 依赖项 | ['com.alibaba.fastjson.JSON', 'com.alibaba.fastjson.JSONObject', 'com.welab.wefe.board.service.dto.entity.AbstractOutputModel', 'com.welab.wefe.common.fieldvalidate.annotation.Check', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.wefe.enums.ComponentType', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'com.welab.wefe.common.wefe.enums.TaskStatus', 'java.util.Date', 'java.util.List'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| TaskResultOutputModel | class |  |



## 类 TaskResultOutputModel

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | TaskResultOutputModel |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| members | List<JObject> |  |
| servingModel | boolean |  |
| result | JSONObject |  |
| position | Integer |  |
| spend | Integer |  |
| flowNodeId | String |  |
| name | String |  |
| finishTime | Date |  |
| taskId | String |  |
| startTime | Date |  |
| role | JobMemberRole |  |
| componentType | ComponentType |  |
| type | String |  |
| errorCause | String |  |
| flowId | String |  |
| jobId | String |  |
| status | TaskStatus |  |
| taskConfig | JSONObject |  |
| message | String |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getName | String |  |
| getTaskId | String |  |
| setFlowNodeId | void |  |
| setMessage | void |  |
| isServingModel | boolean |  |
| getStatus | TaskStatus |  |
| setJobId | void |  |
| setErrorCause | void |  |
| getMembers | List<JObject> |  |
| setMembers | void |  |
| getTaskConfig | JSONObject |  |
| setTaskConfig | void |  |
| getPosition | Integer |  |
| setName | void |  |
| setFinishTime | void |  |
| getMessage | String |  |
| setTaskId | void |  |
| setFlowId | void |  |
| setComponentType | void |  |
| setStatus | void |  |
| setResult | void |  |
| getErrorCause | String |  |
| setServingModel | void |  |
| getRole | JobMemberRole |  |
| setRole | void |  |
| getStartTime | Date |  |
| getComponentType | ComponentType |  |
| getFlowNodeId | String |  |
| setPosition | void |  |
| getResult | JSONObject |  |
| getFlowId | String |  |
| getSpend | Integer |  |
| getType | String |  |
| getFinishTime | Date |  |
| setStartTime | void |  |
| getJobId | String |  |
| setSpend | void |  |
| setType | void |  |




