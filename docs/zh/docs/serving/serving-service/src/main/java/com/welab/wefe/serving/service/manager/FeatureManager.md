# 基础信息

|      |      |
|------|------|
| 名称 | FeatureManager |
| 编码语言 | .java |
| 代码路径 | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/manager/FeatureManager.java |
| 包名 | com.welab.wefe.serving.service.manager |
| 依赖项 | ['com.alibaba.fastjson.JSONObject', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.web.Launcher', 'com.welab.wefe.common.wefe.enums.PredictFeatureDataSource', 'com.welab.wefe.serving.sdk.model.FeatureDataModel', 'com.welab.wefe.serving.service.database.entity.TableModelMySqlModel', 'com.welab.wefe.serving.service.feature.CodeFeatureDataHandler', 'com.welab.wefe.serving.service.feature.SqlFeatureDataHandler', 'com.welab.wefe.serving.service.service.ModelService', 'java.util.HashMap', 'java.util.Map', 'com.welab.wefe.common.StatusCode.UNEXPECTED_ENUM_CASE'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| FeatureManager | class |  |



## 类 FeatureManager

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | FeatureManager |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| modelService | ModelService |  |
| FEATURE_SOURCE = new HashMap<>() | Map<String, PredictFeatureDataSource> |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| refresh | void |  |
| getProcessor | String |  |
| getFeatureSource | PredictFeatureDataSource |  |
| getFeatureData | FeatureDataModel |  |
| getFeatureData | FeatureDataModel |  |




