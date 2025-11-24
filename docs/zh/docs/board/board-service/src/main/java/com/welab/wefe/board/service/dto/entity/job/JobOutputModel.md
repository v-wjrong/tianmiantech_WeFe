# 基础信息

|      |      |
|------|------|
| 名称 | JobOutputModel |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/dto/entity/job/JobOutputModel.java |
| 包名 | com.welab.wefe.board.service.dto.entity.job |
| 依赖项 | ['com.alibaba.fastjson.JSON', 'com.alibaba.fastjson.JSONObject', 'com.welab.wefe.board.service.dto.entity.AbstractOutputModel', 'com.welab.wefe.common.fieldvalidate.annotation.Check', 'com.welab.wefe.common.wefe.enums.FederatedLearningType', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'com.welab.wefe.common.wefe.enums.JobStatus', 'java.util.Date'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| JobOutputModel | class |  |



## 类 JobOutputModel

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | JobOutputModel |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| federatedLearningType | FederatedLearningType |  |
| graph | JSONObject |  |
| flowId | String |  |
| finishTime | Date |  |
| myRole | JobMemberRole |  |
| jobId | String |  |
| star | Boolean |  |
| status | JobStatus |  |
| name | String |  |
| progress | Integer |  |
| hasModelingResult | Boolean |  |
| message | String |  |
| progressUpdatedTime | Date |  |
| startTime | Date |  |
| projectId | String |  |
| remark | String |  |
| statusUpdatedTime | Date |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| setGraph | void |  |
| getStatusUpdatedTime | Date |  |
| getName | String |  |
| getJobId | String |  |
| getStartTime | Date |  |
| setStatusUpdatedTime | void |  |
| getProgressUpdatedTime | Date |  |
| setProgress | void |  |
| setStatus | void |  |
| setStartTime | void |  |
| setMyRole | void |  |
| getMyRole | JobMemberRole |  |
| getFlowId | String |  |
| setProgressUpdatedTime | void |  |
| getStatus | JobStatus |  |
| getProjectId | String |  |
| getFederatedLearningType | FederatedLearningType |  |
| setFinishTime | void |  |
| setFlowId | void |  |
| setName | void |  |
| getGraph | JSONObject |  |
| getFinishTime | Date |  |
| setJobId | void |  |
| getMessage | String |  |
| getProgress | Integer |  |
| setFederatedLearningType | void |  |
| setProjectId | void |  |
| setMessage | void |  |
| getHasModelingResult | Boolean |  |
| setHasModelingResult | void |  |
| getStar | Boolean |  |
| setStar | void |  |
| getRemark | String |  |
| setRemark | void |  |




