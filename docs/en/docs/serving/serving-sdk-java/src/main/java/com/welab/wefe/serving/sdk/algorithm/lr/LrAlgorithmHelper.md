# Basic Information

|      |      |
|------|------|
| Name | LrAlgorithmHelper |
| Language | .java |
| Code Path | WeFe/serving/serving-sdk-java/src/main/java/com/welab/wefe/serving/sdk/algorithm/lr/LrAlgorithmHelper.java |
| Package Name | com.welab.wefe.serving.sdk.algorithm.lr |
| Dependencies | ['com.alibaba.fastjson.JSON', 'com.alibaba.fastjson.util.TypeUtils', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.serving.sdk.dto.BatchPredictParams', 'com.welab.wefe.serving.sdk.enums.StateCode', 'com.welab.wefe.serving.sdk.model.ScoreCardInfoModel', 'com.welab.wefe.serving.sdk.model.lr.LrModel', 'com.welab.wefe.serving.sdk.model.lr.LrPredictResultModel', 'com.welab.wefe.serving.sdk.model.lr.LrScoreCardModel', 'com.welab.wefe.serving.sdk.utils.AlgorithmThreadPool', 'org.apache.commons.compress.utils.Lists', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.math.BigDecimal', 'java.util.List', 'java.util.Map', 'java.util.concurrent.CopyOnWriteArrayList', 'java.util.concurrent.CountDownLatch', 'java.lang.Math.exp'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| LrAlgorithmHelper | class |  |



## Class LrAlgorithmHelper

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | LrAlgorithmHelper |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| LOG = LoggerFactory.getLogger(LrAlgorithmHelper.class) | Logger |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| compute | LrPredictResultModel |  |
| extractWoeArray | List<Double> |  |
| computeScoreCard | LrPredictResultModel |  |
| intercept | Double |  |
| batchCompute | List<LrPredictResultModel> |  |
| computeProbability | LrPredictResultModel |  |
| sigmod | Double |  |
| extractSplitPoints | List<Double> |  |
| getSplitPointIndex | int |  |
| getBinningSplit | String |  |
| precisionProcessByDouble | String |  |




