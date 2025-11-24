# 基础信息

|      |      |
|------|------|
| 名称 | AlgorithmManager |
| 编码语言 | .java |
| 代码路径 | WeFe/serving/serving-sdk-java/src/main/java/com/welab/wefe/serving/sdk/manager/AlgorithmManager.java |
| 包名 | com.welab.wefe.serving.sdk.manager |
| 依赖项 | ['com.welab.wefe.serving.sdk.algorithm.AbstractAlgorithm', 'com.welab.wefe.serving.sdk.algorithm.AbstractBatchAlgorithm', 'com.welab.wefe.serving.sdk.algorithm.lr.batch.LrHorzPromoterBatchAlgorithm', 'com.welab.wefe.serving.sdk.algorithm.lr.batch.LrVertPromoterBatchAlgorithm', 'com.welab.wefe.serving.sdk.algorithm.lr.batch.LrVertProviderBatchAlgorithm', 'com.welab.wefe.serving.sdk.algorithm.lr.single.LrHorzPromoterAlgorithm', 'com.welab.wefe.serving.sdk.algorithm.lr.single.LrVertPromoterAlgorithm', 'com.welab.wefe.serving.sdk.algorithm.lr.single.LrVertProviderAlgorithm', 'com.welab.wefe.serving.sdk.algorithm.xgboost.batch.XgboostHorzPromoterBatchAlgorithm', 'com.welab.wefe.serving.sdk.algorithm.xgboost.batch.XgboostVertPromoterBatchAlgorithm', 'com.welab.wefe.serving.sdk.algorithm.xgboost.batch.XgboostVertProviderBatchAlgorithm', 'com.welab.wefe.serving.sdk.algorithm.xgboost.single.XgboostHorzPromoterAlgorithm', 'com.welab.wefe.serving.sdk.algorithm.xgboost.single.XgboostVertPromoterAlgorithm', 'com.welab.wefe.serving.sdk.algorithm.xgboost.single.XgboostVertProviderAlgorithm', 'com.welab.wefe.serving.sdk.model.BaseModel', 'java.util.HashMap', 'java.util.Map'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| AlgorithmManager | class |  |



## 类 AlgorithmManager

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | AlgorithmManager |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| MAP = new HashMap<>() | Map<String, Class<? extends AbstractAlgorithm>> |  |
| BATCH_MAP = new HashMap<>() | Map<String, Class<? extends AbstractBatchAlgorithm>> |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| get | AbstractAlgorithm |  |
| getBatch | AbstractBatchAlgorithm |  |




