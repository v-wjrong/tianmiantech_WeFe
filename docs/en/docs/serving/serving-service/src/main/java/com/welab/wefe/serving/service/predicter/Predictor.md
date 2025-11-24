# Basic Information

|      |      |
|------|------|
| Name | Predictor |
| Language | .java |
| Code Path | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/predicter/Predictor.java |
| Package Name | com.welab.wefe.serving.service.predicter |
| Dependencies | ['com.alibaba.fastjson.JSONObject', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.web.Launcher', 'com.welab.wefe.common.wefe.enums.FederatedLearningType', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'com.welab.wefe.common.wefe.enums.PredictFeatureDataSource', 'com.welab.wefe.serving.sdk.dto.PredictResult', 'com.welab.wefe.serving.sdk.model.lr.LrPredictResultModel', 'com.welab.wefe.serving.sdk.model.xgboost.XgboostPredictResultModel', 'com.welab.wefe.serving.sdk.predicter.AbstractBasePredictor', 'com.welab.wefe.serving.service.database.entity.ModelMemberMySqlModel', 'com.welab.wefe.serving.service.database.entity.TableModelMySqlModel', 'com.welab.wefe.serving.service.dto.ServiceResultOutput', 'com.welab.wefe.serving.service.predicter.batch.BatchPromoterPredictor', 'com.welab.wefe.serving.service.predicter.batch.BatchProviderPredictor', 'com.welab.wefe.serving.service.predicter.single.DebugPromoterPredictor', 'com.welab.wefe.serving.service.predicter.single.DebugProviderPredictor', 'com.welab.wefe.serving.service.predicter.single.PromoterPredictor', 'com.welab.wefe.serving.service.predicter.single.ProviderPredictor', 'com.welab.wefe.serving.service.service.CacheObjects', 'com.welab.wefe.serving.service.service.ModelMemberService', 'com.welab.wefe.serving.service.service.ModelPredictScoreStatisticsService', 'com.welab.wefe.serving.service.service.ModelService', 'org.apache.commons.collections4.CollectionUtils', 'java.util.List', 'java.util.Map'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| Predictor | class |  |



## Class Predictor

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | Predictor |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| modelService | ModelService |  |
| modelMemberService | ModelMemberService |  |
| modelPredictScoreStatisticsService | ModelPredictScoreStatisticsService |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| batch | PredictResult |  |
| makeSensitiveData | void |  |
| recordPredictScoreIncrement | void |  |
| predict | PredictResult |  |
| constructPredictor | AbstractBasePredictor |  |
| constructPredictor | AbstractBasePredictor |  |
| findMyRole | JobMemberRole |  |
| findFlType | FederatedLearningType |  |
| debug | PredictResult |  |
| constructDebugPredictor | AbstractBasePredictor |  |




