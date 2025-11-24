# Basic Information

|      |      |
|------|------|
| Name | PredictLogMySqlModel |
| Language | .java |
| Code Path | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/database/entity/PredictLogMySqlModel.java |
| Package Name | com.welab.wefe.serving.service.database.entity |
| Dependencies | ['com.welab.wefe.common.wefe.enums.Algorithm', 'com.welab.wefe.common.wefe.enums.FederatedLearningType', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'javax.persistence', 'java.util.Date', 'java.util.UUID'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| PredictLogMySqlModel | class |  |



## Class PredictLogMySqlModel

|      |      |
|------|------|
| Access Modifier | @Entity(name = "predict_log");public |
| Type | class |
| Name | PredictLogMySqlModel |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| id = UUID.randomUUID().toString().replaceAll("-", "") | String |  |
| result | boolean |  |
| memberId | String |  |
| response | String |  |
| modelId | String |  |
| createdTime = new Date() | Date |  |
| seqNo | String |  |
| spend | long |  |
| myRole | JobMemberRole |  |
| algorithm | Algorithm |  |
| flType | FederatedLearningType |  |
| request | String |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| setModelId | void |  |
| getCreatedTime | Date |  |
| getId | String |  |
| setResponse | void |  |
| setFlType | void |  |
| setCreatedTime | void |  |
| getModelId | String |  |
| isResult | boolean |  |
| getMemberId | String |  |
| setAlgorithm | void |  |
| setResult | void |  |
| getRequest | String |  |
| getResponse | String |  |
| setRequest | void |  |
| setSeqNo | void |  |
| getSeqNo | String |  |
| getSpend | long |  |
| setMemberId | void |  |
| setMyRole | void |  |
| setId | void |  |
| setSpend | void |  |
| getMyRole | JobMemberRole |  |
| getAlgorithm | Algorithm |  |
| getFlType | FederatedLearningType |  |




