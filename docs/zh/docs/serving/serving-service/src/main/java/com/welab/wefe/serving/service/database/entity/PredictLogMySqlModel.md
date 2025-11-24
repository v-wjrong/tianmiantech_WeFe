# 基础信息

|      |      |
|------|------|
| 名称 | PredictLogMySqlModel |
| 编码语言 | .java |
| 代码路径 | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/database/entity/PredictLogMySqlModel.java |
| 包名 | com.welab.wefe.serving.service.database.entity |
| 依赖项 | ['com.welab.wefe.common.wefe.enums.Algorithm', 'com.welab.wefe.common.wefe.enums.FederatedLearningType', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'javax.persistence', 'java.util.Date', 'java.util.UUID'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| PredictLogMySqlModel | class |  |



## 类 PredictLogMySqlModel

|      |      |
|------|------|
| 访问范围 | @Entity(name = "predict_log");public |
| 类型 | class |
| 名称 | PredictLogMySqlModel |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
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

### 方法列表

| 名称  | 类型  | 说明 |
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




