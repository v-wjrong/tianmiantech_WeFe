# 基础信息

|      |      |
|------|------|
| 名称 | XgboostPmmlLanguage |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/modelexport/XgboostPmmlLanguage.java |
| 包名 | com.welab.wefe.board.service.service.modelexport |
| 依赖项 | ['com.welab.wefe.common.util.JObject', 'org.dmg.pmml', 'org.dmg.pmml.mining.MiningModel', 'org.dmg.pmml.mining.Segment', 'org.dmg.pmml.mining.Segmentation', 'org.dmg.pmml.regression.NumericPredictor', 'org.dmg.pmml.regression.RegressionModel', 'org.dmg.pmml.regression.RegressionTable', 'org.dmg.pmml.tree.TreeModel', 'org.jpmml.model.PMMLUtil', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.io.ByteArrayOutputStream', 'java.util.HashSet', 'java.util.List', 'java.util.Map', 'java.util.Set'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| XgboostPmmlLanguage | class |  |



## 类 XgboostPmmlLanguage

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | XgboostPmmlLanguage |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| LOG = LoggerFactory.getLogger(this.getClass()) | Logger |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| buildSegmentation | Segmentation |  |
| buildMiningModel | MiningModel |  |
| buildLocalTransformations | LocalTransformations |  |
| buildMiningSchema | MiningSchema |  |
| buildOutput | Output |  |
| buildTopMiningModel | MiningModel |  |
| buildTreeLogicSegment | Segment |  |
| buildMiningBuildTask | MiningBuildTask |  |
| buildDataDictionary | DataDictionary |  |
| buildHeader | Header |  |
| buildWholeCode | String |  |
| buildClassificationSegmen | Segment |  |
| buildTopSegmentation | Segmentation |  |
| buildTreeSegment | Segment |  |
| buildInitScoreSegment | Segment |  |
| buildTreeModel | TreeModel |  |
| buildTreeModelMiningSchema | MiningSchema |  |
| buildNode | void |  |




