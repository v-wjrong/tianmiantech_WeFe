# Basic Information

|      |      |
|------|------|
| Name | BatchPromoterPredictor |
| Language | .java |
| Code Path | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/predicter/batch/BatchPromoterPredictor.java |
| Package Name | com.welab.wefe.serving.service.predicter.batch |
| Dependencies | ['com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.web.Launcher', 'com.welab.wefe.serving.sdk.dto.ProviderParams', 'com.welab.wefe.serving.sdk.model.BaseModel', 'com.welab.wefe.serving.sdk.model.FeatureDataModel', 'com.welab.wefe.serving.sdk.predicter.batch.AbstractBatchPredictor', 'com.welab.wefe.serving.service.manager.FeatureManager', 'com.welab.wefe.serving.service.manager.ModelManager', 'com.welab.wefe.serving.service.predicter.single.PromoterPredictHelper', 'com.welab.wefe.serving.service.service.ClientServiceService', 'org.apache.commons.collections4.CollectionUtils', 'org.apache.commons.collections4.MapUtils', 'java.util.ArrayList', 'java.util.List', 'java.util.Map'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| BatchPromoterPredictor | class |  |



## Class BatchPromoterPredictor

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | BatchPromoterPredictor |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| requestId | String |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getModel | BaseModel |  |
| federatedResultByProviders | List<JObject> |  |
| findFeatureData | FeatureDataModel |  |




