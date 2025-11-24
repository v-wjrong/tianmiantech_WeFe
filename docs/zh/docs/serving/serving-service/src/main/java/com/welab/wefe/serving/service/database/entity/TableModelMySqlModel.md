# 基础信息

|      |      |
|------|------|
| 名称 | TableModelMySqlModel |
| 编码语言 | .java |
| 代码路径 | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/database/entity/TableModelMySqlModel.java |
| 包名 | com.welab.wefe.serving.service.database.entity |
| 依赖项 | ['com.welab.wefe.common.wefe.enums.Algorithm', 'com.welab.wefe.common.wefe.enums.FederatedLearningType', 'com.welab.wefe.common.wefe.enums.PredictFeatureDataSource', 'javax.persistence'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| TableModelMySqlModel | class |  |



## 类 TableModelMySqlModel

|      |      |
|------|------|
| 访问范围 | @Entity(name = "table_model");@Table(name = "table_model");public |
| 类型 | class |
| 名称 | TableModelMySqlModel |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| sqlScript | String |  |
| algorithm | Algorithm |  |
| dataSourceId | String |  |
| filename | String |  |
| modelParam | String |  |
| sqlConditionField | String |  |
| scoresDistribution | String |  |
| flType | FederatedLearningType |  |
| sourcePath | String |  |
| serialVersionUID = -1320731560182386318L | long |  |
| featureSource = PredictFeatureDataSource.code | PredictFeatureDataSource |  |
| useCount | int |  |
| scoreCardInfo | String |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getFilename | String |  |
| setSqlScript | void |  |
| setFilename | void |  |
| getSqlScript | String |  |
| getDataSourceId | String |  |
| getFeatureSource | PredictFeatureDataSource |  |
| setUseCount | void |  |
| setDataSourceId | void |  |
| getModelParam | String |  |
| getFlType | FederatedLearningType |  |
| setSqlConditionField | void |  |
| getScoresDistribution | String |  |
| getAlgorithm | Algorithm |  |
| getScoreCardInfo | String |  |
| setScoreCardInfo | void |  |
| setModelParam | void |  |
| setAlgorithm | void |  |
| getSqlConditionField | String |  |
| setSourcePath | void |  |
| setScoresDistribution | void |  |
| setFeatureSource | void |  |
| setFlType | void |  |
| getUseCount | int |  |
| getSourcePath | String |  |




