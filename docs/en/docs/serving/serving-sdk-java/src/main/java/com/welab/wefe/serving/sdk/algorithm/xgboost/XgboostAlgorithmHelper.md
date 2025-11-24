# Basic Information

|      |      |
|------|------|
| Name | XgboostAlgorithmHelper |
| Language | .java |
| Code Path | WeFe/serving/serving-sdk-java/src/main/java/com/welab/wefe/serving/sdk/algorithm/xgboost/XgboostAlgorithmHelper.java |
| Package Name | com.welab.wefe.serving.sdk.algorithm.xgboost |
| Dependencies | ['java.lang.Math.exp', 'java.math.BigDecimal', 'java.util.ArrayList', 'java.util.HashMap', 'java.util.Map', 'org.apache.commons.collections4.MapUtils', 'org.apache.commons.lang3.ObjectUtils', 'com.alibaba.fastjson.util.TypeUtils', 'com.welab.wefe.serving.sdk.enums.XgboostWorkMode', 'com.welab.wefe.serving.sdk.model.xgboost.XgbProviderPredictResultModel', 'com.welab.wefe.serving.sdk.model.xgboost.XgboostDecisionTreeModel', 'com.welab.wefe.serving.sdk.model.xgboost.XgboostModel', 'com.welab.wefe.serving.sdk.model.xgboost.XgboostNodeModel', 'com.welab.wefe.serving.sdk.model.xgboost.XgboostPredictResultModel'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| XgboostAlgorithmHelper | class |  |



## Class XgboostAlgorithmHelper

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | XgboostAlgorithmHelper |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| PROVIDER = "provider" | String |  |
| COMPARING_VALUES = BigDecimal.valueOf(1e-17) | BigDecimal |  |
| PROMOTER = "promoter" | String |  |
| CATEGORY = 2 | int |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getSite | String |  |
| providerDecision | int |  |
| providerPredict | XgbProviderPredictResultModel |  |
| finalPredict | Object |  |
| getNextNodeId | int |  |
| nextTreeNodeIdByHorz | int |  |
| softmax | Map<String, Object> |  |
| decision | int |  |
| federatedDecision | int |  |
| skipPredictModel | XgboostPredictResultModel |  |
| promoterPredictByHorz | XgboostPredictResultModel |  |
| isLeaf | boolean |  |
| promoterPredictByVert | XgboostPredictResultModel |  |
| getTreeLeafWeight | double |  |
| skipProviderPredictModel | XgbProviderPredictResultModel |  |
| sigmod | double |  |
| nextTreeNodeIdByVert | int |  |




