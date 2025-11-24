# 基础信息

|      |      |
|------|------|
| 名称 | XgboostAlgorithmHelper |
| 编码语言 | .java |
| 代码路径 | WeFe/serving/serving-sdk-java/src/main/java/com/welab/wefe/serving/sdk/algorithm/xgboost/XgboostAlgorithmHelper.java |
| 包名 | com.welab.wefe.serving.sdk.algorithm.xgboost |
| 依赖项 | ['java.lang.Math.exp', 'java.math.BigDecimal', 'java.util.ArrayList', 'java.util.HashMap', 'java.util.Map', 'org.apache.commons.collections4.MapUtils', 'org.apache.commons.lang3.ObjectUtils', 'com.alibaba.fastjson.util.TypeUtils', 'com.welab.wefe.serving.sdk.enums.XgboostWorkMode', 'com.welab.wefe.serving.sdk.model.xgboost.XgbProviderPredictResultModel', 'com.welab.wefe.serving.sdk.model.xgboost.XgboostDecisionTreeModel', 'com.welab.wefe.serving.sdk.model.xgboost.XgboostModel', 'com.welab.wefe.serving.sdk.model.xgboost.XgboostNodeModel', 'com.welab.wefe.serving.sdk.model.xgboost.XgboostPredictResultModel'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| XgboostAlgorithmHelper | class |  |



## 类 XgboostAlgorithmHelper

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | XgboostAlgorithmHelper |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| PROVIDER = "provider" | String |  |
| COMPARING_VALUES = BigDecimal.valueOf(1e-17) | BigDecimal |  |
| PROMOTER = "promoter" | String |  |
| CATEGORY = 2 | int |  |

### 方法列表

| 名称  | 类型  | 说明 |
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




