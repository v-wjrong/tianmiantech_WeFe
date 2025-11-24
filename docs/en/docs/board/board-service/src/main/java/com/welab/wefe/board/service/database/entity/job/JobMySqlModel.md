# Basic Information

|      |      |
|------|------|
| Name | JobMySqlModel |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/database/entity/job/JobMySqlModel.java |
| Package Name | com.welab.wefe.board.service.database.entity.job |
| Dependencies | ['com.alibaba.fastjson.JSONObject', 'com.vladmihalcea.hibernate.type.json.JsonStringType', 'com.welab.wefe.board.service.database.entity.base.AbstractBaseMySqlModel', 'com.welab.wefe.board.service.dto.kernel.machine_learning.KernelJob', 'com.welab.wefe.common.wefe.enums.FederatedLearningType', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'com.welab.wefe.common.wefe.enums.JobStatus', 'org.hibernate.annotations.Type', 'org.hibernate.annotations.TypeDef', 'javax.persistence.Column', 'javax.persistence.Entity', 'javax.persistence.EnumType', 'javax.persistence.Enumerated', 'java.util.Date'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| JobMySqlModel | class |  |



## Class JobMySqlModel

|      |      |
|------|------|
| Access Modifier | @Entity(name = "job");@TypeDef(name = "json", typeClass = JsonStringType.class);public |
| Type | class |
| Name | JobMySqlModel |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
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

### Method List

| Name  | Type  | Description |
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




