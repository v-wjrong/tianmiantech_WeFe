# 基础信息

|      |      |
|------|------|
| 名称 | BatchPredictParams |
| 编码语言 | .java |
| 代码路径 | WeFe/serving/serving-sdk-java/src/main/java/com/welab/wefe/serving/sdk/dto/BatchPredictParams.java |
| 包名 | com.welab.wefe.serving.sdk.dto |
| 依赖项 | ['org.apache.commons.collections4.MapUtils', 'org.apache.commons.compress.utils.Lists', 'java.util.Collections', 'java.util.List', 'java.util.Map', 'java.util.stream.Collectors'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| BatchPredictParams | class |  |



## 类 BatchPredictParams

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | BatchPredictParams |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| predictParamsList = Lists.newArrayList() | List<PredictParams> |  |
| userIds = Lists.newArrayList() | List<String> |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getPredictParamsList | List<PredictParams> |  |
| initializePredictParamsList | void |  |
| create | BatchPredictParams |  |
| replacePredictParamsList | void |  |
| getUserIds | List<String> |  |
| getPredictParamsByUserId | PredictParams |  |




