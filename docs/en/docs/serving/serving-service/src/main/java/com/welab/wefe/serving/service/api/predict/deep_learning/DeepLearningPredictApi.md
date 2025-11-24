# Basic Information

|      |      |
|------|------|
| Name | DeepLearningPredictApi |
| Language | .java |
| Code Path | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/api/predict/deep_learning/DeepLearningPredictApi.java |
| Package Name | com.welab.wefe.serving.service.api.predict.deep_learning |
| Dependencies | ['com.welab.wefe.common.fieldvalidate.annotation.Check', 'com.welab.wefe.common.file.decompression.SuperDecompressor', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.web.api.base.AbstractApi', 'com.welab.wefe.common.web.api.base.Api', 'com.welab.wefe.common.web.dto.AbstractApiInput', 'com.welab.wefe.common.web.dto.ApiResult', 'com.welab.wefe.serving.service.utils.DeepLearningUtil', 'com.welab.wefe.serving.service.utils.ServingFileUtil', 'java.io.File', 'java.nio.file.Path'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| DeepLearningPredictApi | class |  |



## Class DeepLearningPredictApi

|      |      |
|------|------|
| Access Modifier | @Api(;        path = "predict/deep_learning",;        name = "深度学习预测",;        login = false;);public |
| Type | class |
| Name | DeepLearningPredictApi |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getWordDir | String |  |
| handle | ApiResult<String> |  |
| unZipModelFile | void |  |




