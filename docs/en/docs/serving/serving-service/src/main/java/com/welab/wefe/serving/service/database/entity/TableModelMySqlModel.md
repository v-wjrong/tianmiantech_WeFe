# Basic Information

|      |      |
|------|------|
| Name | TableModelMySqlModel |
| Language | .java |
| Code Path | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/database/entity/TableModelMySqlModel.java |
| Package Name | com.welab.wefe.serving.service.database.entity |
| Dependencies | ['com.welab.wefe.common.wefe.enums.Algorithm', 'com.welab.wefe.common.wefe.enums.FederatedLearningType', 'com.welab.wefe.common.wefe.enums.PredictFeatureDataSource', 'javax.persistence'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| TableModelMySqlModel | class |  |



## Class TableModelMySqlModel

|      |      |
|------|------|
| Access Modifier | @Entity(name = "table_model");@Table(name = "table_model");public |
| Type | class |
| Name | TableModelMySqlModel |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
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

### Method List

| Name  | Type  | Description |
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




