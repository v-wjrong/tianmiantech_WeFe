# Basic Information

|      |      |
|------|------|
| Name | Components |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/component/Components.java |
| Package Name | com.welab.wefe.board.service.component |
| Dependencies | ['com.welab.wefe.board.service.component.base.AbstractComponent', 'com.welab.wefe.board.service.component.deep_learning.ImageDataIOComponent', 'com.welab.wefe.board.service.component.deep_learning.PaddleClassifyComponent', 'com.welab.wefe.board.service.component.deep_learning.PaddleDetectionComponent', 'com.welab.wefe.board.service.component.feature', 'com.welab.wefe.board.service.component.modeling', 'com.welab.wefe.common.web.Launcher', 'com.welab.wefe.common.wefe.enums.ComponentType', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.stereotype.Service'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| Components | class |  |



## Class Components

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | Components |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| featurePsiComponent | FeaturePsiComponent |  |
| segmentComponent | SegmentComponent |  |
| mixSecureBoostComponent | MixSecureBoostComponent |  |
| mixLrComponent | MixLrComponent |  |
| ootComponent | OotComponent |  |
| vertPearsonComponent | VertPearsonComponent |  |
| vertOneHotComponent | VertOneHotComponent |  |
| horzNNComponent | HorzNNComponent |  |
| featureSelectionComponent | FeatureSelectionComponent |  |
| horzLRComponent | HorzLRComponent |  |
| featureCalculationComponent | FeatureCalculationComponent |  |
| vertPCAComponent | VertPCAComponent |  |
| dataIOComponent | DataIOComponent |  |
| horzStatisticComponent | HorzStatisticComponent |  |
| horzSecureBoostComponent | HorzSecureBoostComponent |  |
| featureStatisticsComponent | FeatureStatisticsComponent |  |
| paddleDetectionComponent | PaddleDetectionComponent |  |
| scoreCardComponent | ScoreCardComponent |  |
| binningComponent | BinningComponent |  |
| imageDataIOComponent | ImageDataIOComponent |  |
| vertLRComponent | VertLRComponent |  |
| intersectionComponent | IntersectionComponent |  |
| mixBinningComponent | MixBinningComponent |  |
| vertNNComponent | VertNNComponent |  |
| featureTransformComponent | FeatureTransformComponent |  |
| fillMissingValueComponent | FillMissingValueComponent |  |
| mixStatisticComponent | MixStatisticComponent |  |
| horzOneHotComponent | HorzOneHotComponent |  |
| featureStandardizedComponent | FeatureStandardizedComponent |  |
| horzFeatureBinningComponent | HorzFeatureBinningComponent |  |
| vertFilterComponent | VertFilterComponent |  |
| vertSecureBoostComponent | VertSecureBoostComponent |  |
| paddleClassifyComponent | PaddleClassifyComponent |  |
| evaluationComponent | EvaluationComponent |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getDataIOComponent | AbstractComponent<?> |  |
| get | AbstractComponent<?> |  |
| needArbiterTask | boolean |  |




