# 基础信息

|      |      |
|------|------|
| 名称 | JobMySqlModel |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/database/entity/job/JobMySqlModel.java |
| 包名 | com.welab.wefe.board.service.database.entity.job |
| 依赖项 | ['com.alibaba.fastjson.JSONObject', 'com.vladmihalcea.hibernate.type.json.JsonStringType', 'com.welab.wefe.board.service.database.entity.base.AbstractBaseMySqlModel', 'com.welab.wefe.board.service.dto.kernel.machine_learning.KernelJob', 'com.welab.wefe.common.wefe.enums.FederatedLearningType', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'com.welab.wefe.common.wefe.enums.JobStatus', 'org.hibernate.annotations.Type', 'org.hibernate.annotations.TypeDef', 'javax.persistence.Column', 'javax.persistence.Entity', 'javax.persistence.EnumType', 'javax.persistence.Enumerated', 'java.util.Date'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| JobMySqlModel | class |  |



## 类 JobMySqlModel

|      |      |
|------|------|
| 访问范围 | @Entity(name = "job");@TypeDef(name = "json", typeClass = JsonStringType.class);public |
| 类型 | class |
| 名称 | JobMySqlModel |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| status | JobStatus |  |
| hasModelingResult | boolean |  |
| progressUpdatedTime | Date |  |
| jobConfig | JSONObject |  |
| message | String |  |
| federatedLearningType | FederatedLearningType |  |
| projectId | String |  |
| flowId | String |  |
| star | boolean |  |
| graph | String |  |
| serialVersionUID = 8933206598650203308L | long |  |
| progress | Integer |  |
| finishTime | Date |  |
| remark | String |  |
| startTime | Date |  |
| jobId | String |  |
| myRole | JobMemberRole |  |
| statusUpdatedTime | Date |  |
| name | String |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| setProjectId | void |  |
| getProjectId | String |  |
| isHasModelingResult | boolean |  |
| setMyRole | void |  |
| setFederatedLearningType | void |  |
| getStatus | JobStatus |  |
| setJobId | void |  |
| getStatusUpdatedTime | Date |  |
| setRemark | void |  |
| getMessage | String |  |
| setStartTime | void |  |
| getName | String |  |
| getJobId | String |  |
| getProgressUpdatedTime | Date |  |
| getMyRole | JobMemberRole |  |
| isStar | boolean |  |
| getFinishTime | Date |  |
| setMessage | void |  |
| getStartTime | Date |  |
| getRemark | String |  |
| setStar | void |  |
| setHasModelingResult | void |  |
| setStatus | void |  |
| setName | void |  |
| setProgressUpdatedTime | void |  |
| setProgress | void |  |
| setFlowId | void |  |
| getFederatedLearningType | FederatedLearningType |  |
| setStatusUpdatedTime | void |  |
| setFinishTime | void |  |
| setJobConfig | void |  |
| setGraph | void |  |
| getFlowId | String |  |
| getGraph | String |  |
| getProgress | Integer |  |
| getJobConfig | JSONObject |  |
| setJobConfig | void |  |




