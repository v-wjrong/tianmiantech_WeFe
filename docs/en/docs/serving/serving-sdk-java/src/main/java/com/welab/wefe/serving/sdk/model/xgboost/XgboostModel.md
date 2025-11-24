# Basic Information

|      |      |
|------|------|
| Name | XgboostModel |
| Language | .java |
| Code Path | WeFe/serving/serving-sdk-java/src/main/java/com/welab/wefe/serving/sdk/model/xgboost/XgboostModel.java |
| Package Name | com.welab.wefe.serving.sdk.model.xgboost |
| Dependencies | ['java.util.HashMap', 'java.util.List', 'java.util.Map'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| XgboostModel | class |  |



## Class XgboostModel

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | XgboostModel |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
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

### Method List

| Name  | Type  | Description |
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




