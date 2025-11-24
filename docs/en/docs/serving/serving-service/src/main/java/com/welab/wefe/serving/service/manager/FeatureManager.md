# Basic Information

|      |      |
|------|------|
| Name | FeatureManager |
| Language | .java |
| Code Path | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/manager/FeatureManager.java |
| Package Name | com.welab.wefe.serving.service.manager |
| Dependencies | ['com.alibaba.fastjson.JSONObject', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.web.Launcher', 'com.welab.wefe.common.wefe.enums.PredictFeatureDataSource', 'com.welab.wefe.serving.sdk.model.FeatureDataModel', 'com.welab.wefe.serving.service.database.entity.TableModelMySqlModel', 'com.welab.wefe.serving.service.feature.CodeFeatureDataHandler', 'com.welab.wefe.serving.service.feature.SqlFeatureDataHandler', 'com.welab.wefe.serving.service.service.ModelService', 'java.util.HashMap', 'java.util.Map', 'com.welab.wefe.common.StatusCode.UNEXPECTED_ENUM_CASE'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| FeatureManager | class |  |



## Class FeatureManager

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | FeatureManager |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| modelService | ModelService |  |
| FEATURE_SOURCE = new HashMap<>() | Map<String, PredictFeatureDataSource> |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| refresh | void |  |
| getProcessor | String |  |
| getFeatureSource | PredictFeatureDataSource |  |
| getFeatureData | FeatureDataModel |  |
| getFeatureData | FeatureDataModel |  |




