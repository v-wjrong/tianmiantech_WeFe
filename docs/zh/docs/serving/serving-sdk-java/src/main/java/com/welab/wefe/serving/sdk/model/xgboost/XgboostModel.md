# 基础信息

|      |      |
|------|------|
| 名称 | XgboostModel |
| 编码语言 | .java |
| 代码路径 | WeFe/serving/serving-sdk-java/src/main/java/com/welab/wefe/serving/sdk/model/xgboost/XgboostModel.java |
| 包名 | com.welab.wefe.serving.sdk.model.xgboost |
| 依赖项 | ['java.util.HashMap', 'java.util.List', 'java.util.Map'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| XgboostModel | class |  |



## 类 XgboostModel

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | XgboostModel |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| learningRate | double |  |
| treeDim | int |  |
| classes | List<String> |  |
| initScore | List<Double> |  |
| fastMode = true | boolean |  |
| trees | List<XgboostDecisionTreeModel> |  |
| numClasses | int |  |
| treeNum | int |  |
| featureNameFidMapping = new HashMap<>() | Map<String, String> |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| setFastMode | void |  |
| isFastMode | boolean |  |
| setLearningRate | void |  |
| getTreeDim | int |  |
| getFeatureNameFidMapping | Map<String, String> |  |
| setNumClasses | void |  |
| setTrees | void |  |
| getTrees | List<XgboostDecisionTreeModel> |  |
| setInitScore | void |  |
| getTreeNum | int |  |
| setFeatureNameFidMapping | void |  |
| getInitScore | List<Double> |  |
| getNumClasses | int |  |
| setTreeNum | void |  |
| setTreeDim | void |  |
| setClasses | void |  |
| getClasses | List<String> |  |
| getLearningRate | double |  |




