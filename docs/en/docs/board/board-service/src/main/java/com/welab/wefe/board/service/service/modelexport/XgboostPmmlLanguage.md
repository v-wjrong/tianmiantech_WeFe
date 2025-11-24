# Basic Information

|      |      |
|------|------|
| Name | XgboostPmmlLanguage |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/modelexport/XgboostPmmlLanguage.java |
| Package Name | com.welab.wefe.board.service.service.modelexport |
| Dependencies | ['com.welab.wefe.common.util.JObject', 'org.dmg.pmml', 'org.dmg.pmml.mining.MiningModel', 'org.dmg.pmml.mining.Segment', 'org.dmg.pmml.mining.Segmentation', 'org.dmg.pmml.regression.NumericPredictor', 'org.dmg.pmml.regression.RegressionModel', 'org.dmg.pmml.regression.RegressionTable', 'org.dmg.pmml.tree.TreeModel', 'org.jpmml.model.PMMLUtil', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.io.ByteArrayOutputStream', 'java.util.HashSet', 'java.util.List', 'java.util.Map', 'java.util.Set'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| XgboostPmmlLanguage | class |  |



## Class XgboostPmmlLanguage

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | XgboostPmmlLanguage |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| LOG = LoggerFactory.getLogger(this.getClass()) | Logger |  |

### Method List

| Name  | Type  | Description |
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




