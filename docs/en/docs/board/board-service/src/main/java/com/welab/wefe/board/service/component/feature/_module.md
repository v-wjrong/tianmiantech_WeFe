# Basic Information

|      |      |
|------|------|
| Name | feature |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/component/feature |
| Package Name | docs.board.board-service.src.main.java.com.welab.wefe.board.service.component.feature |
| Brief Description | The HorzFeatureBinningComponent implements horizontal feature binning, supporting equal frequency, equal width, and chi-square methods. The FeatureTransformComponent handles feature transformation tasks. The VertFilterComponent manages vertical filtering tasks. The MixBinningComponent processes mixed binning. The FeatureStandardizedComponent standardizes features. The MixStatisticComponent deals with mixed statistics. The BinningComponent implements binning functionality. The HorzOneHotComponent handles horizontal one-hot encoding. The FillMissingValueComponent fills missing values. The FeatureStatisticsComponent manages feature statistics. The HorzStatisticComponent processes horizontal statistics. The VertOneHotComponent handles vertical one-hot encoding. The VertPCAComponent implements vertical PCA. The VertPearsonComponent calculates Pearson correlation. The FeaturePsiComponent manages feature PSI operations. The FeatureSelectionComponent is used for feature selection. |

# Description

## Overview  
This module is a set of Spring service components focused on feature engineering processing in federated learning, akin to a data preprocessing pipeline. Its core responsibilities include feature binning (equal frequency/equal width/chi-square), standardization, one-hot encoding, missing value imputation, statistical analysis, and PSI calculation. All components inherit from `AbstractComponent` and adhere to a unified interface specification: parameter validation (e.g., participant member checks), task parameter generation (JSON format), and result processing (model/dataset output).  

Key data structures include three nested classes—`Params` (task configuration), `Member` (member information), and `Feature` (feature attributes)—which support feature selection functionality. External dependencies are concentrated on the `DataSetInstance` input/output type, with some components requiring prior `DataIO` or sample alignment nodes. For example, `HorzFeatureBinningComponent` relies on a binning model, while `VertPCAComponent` requires a sample alignment component.  

## Primary Business Scenarios  
The module supports feature processing in horizontal, vertical, and hybrid federated scenarios. A typical workflow involves: first validating member participation and preconditions (e.g., `FeaturePsiComponent` requires a binary classification dataset), then generating task parameters with feature rules (e.g., `MixBinningComponent` configures binning methods), and finally outputting processed datasets or statistical results (JSON format).  

The interaction mode uniformly adopts a "validation-parameterization-execution" chain. For instance, `FillMissingValueComponent` first verifies full member participation before generating imputation strategy parameters. API types cover feature transformation (`FeatureTransformComponent`), filtering (`VertFilterComponent`), and statistical analysis (`HorzStatisticComponent`). Integration examples include: feature binning followed by one-hot encoding (`HorzOneHotComponent`), or PSI calculation requiring sample alignment (`FeaturePsiComponent`).


### Package Internal Structure View

```mermaid
graph TD
    feature --> HorzFeatureBinningComponent.java
    feature --> FeatureTransformComponent.java
    feature --> VertFilterComponent.java
    feature --> MixBinningComponent.java
    feature --> FeatureStandardizedComponent.java
    feature --> MixStatisticComponent.java
    feature --> BinningComponent.java
    feature --> HorzOneHotComponent.java
    feature --> FillMissingValueComponent.java
    feature --> FeatureStatisticsComponent.java
    feature --> HorzStatisticComponent.java
    feature --> VertOneHotComponent.java
    feature --> VertPCAComponent.java
    feature --> VertPearsonComponent.java
    feature --> FeatureCalculationComponent.java
    feature --> FeaturePsiComponent.java
    feature --> FeatureSelectionComponent.java
```

This flowchart displays 17 Java component files under the feature directory, all of which are implementation classes directly located within the feature directory without deeper subdirectory structures. The component files are named after feature processing-related functionalities, covering various data processing capabilities such as feature binning, transformation, standardization, and statistical calculations.

# File List

| Name   | Type  | Description |
|-------|------|-------------|
| [HorzFeatureBinningComponent.java](HorzFeatureBinningComponent.md) | file | The HorzFeatureBinningComponent implements feature binning functionality, checks member participation, generates binning parameters, and supports equal frequency, equal width, and chi-square binning methods, outputting the binning model and dataset. |
| [FeatureTransformComponent.java](FeatureTransformComponent.md) | file | Feature transformation component, inherits from an abstract class, handles feature transformation tasks. Includes parameter validation, task parameter generation, and input/output definitions. Supports feature selection and transformation rule configuration, returns the transformed dataset. |
| [VertFilterComponent.java](VertFilterComponent.md) | file | The VertFilterComponent is a service component designed to handle vertical filtering tasks. It inherits from AbstractComponent and includes functionalities such as parameter validation, task parameter creation, and input/output definitions. The Params class defines parameters including member information and filtering rules. |
| [MixBinningComponent.java](MixBinningComponent.md) | file | The MixBinningComponent is a component that handles binning strategies, checks member participation, and generates binning parameters, supporting various binning methods such as equal frequency, equal width, and chi-square. |
| [FeatureStandardizedComponent.java](FeatureStandardizedComponent.md) | file | The FeatureStandardizedComponent is a feature standardization component that inherits from AbstractComponent. It checks the DataIO component and extracts the with_label field, processes member feature information, supports z-score or min-max standardization methods, and outputs a standardized dataset. |
| [MixStatisticComponent.java](MixStatisticComponent.md) | file | The MixStatisticComponent is a component that handles mixed statistics, inheriting from AbstractComponent. It supports feature selection, generates JSON results, and contains logic for member feature processing and result reorganization. |
| [BinningComponent.java](BinningComponent.md) | file | The BinningComponent is a binning processing component that inherits from AbstractComponent, encompassing parameter validation, task parameter construction, and result processing functionalities. It supports various binning methods such as equal frequency, equal width, optimal binning, and custom binning, ensuring all members participate and generating both binning models and datasets. |
| [HorzOneHotComponent.java](HorzOneHotComponent.md) | file | The HorzOneHotComponent implements horizontal OneHot encoding, checks member features, and generates task parameters, supporting feature selection with dataset instances as input and output. |
| [FillMissingValueComponent.java](FillMissingValueComponent.md) | file | The FillMissingValueComponent is a component designed for handling missing value imputation, which checks member participation status, generates task parameters, and supports feature selection and dataset saving. |
| [FeatureStatisticsComponent.java](FeatureStatisticsComponent.md) | file | The FeatureStatisticsComponent is a component designed for feature statistics, which checks the participation of data IO members and supports both local and distributed modes, outputting results in JSON format. |
| [HorzStatisticComponent.java](HorzStatisticComponent.md) | file | The HorzStatisticComponent is a component designed for handling horizontal statistical tasks, supporting feature selection, generating JSON results, and including member feature processing and result formatting functionalities. |
| [VertOneHotComponent.java](VertOneHotComponent.md) | file | VertOneHotComponent inherits from AbstractComponent, implements feature transformation logic, supports feature selection, with dataset instances as input and output. |
| [VertPCAComponent.java](VertPCAComponent.md) | file | VertPCAComponent is a vertical PCA component that checks pre-sample alignment and ensures the number of members does not exceed two parties. It generates feature list task parameters, takes a dataset as input, and outputs JSON results. |
| [VertPearsonComponent.java](VertPearsonComponent.md) | file | The VertPearsonComponent is a component designed for calculating Pearson correlation, requiring no more than two parties as members and necessitating prior sample alignment and the DataIO component. It supports feature selection and cross-party computation, outputting results in JSON format. |
| [FeatureCalculationComponent.java](FeatureCalculationComponent.md) | file | The FeatureCalculationComponent is deprecated. It is recommended to use the Feature Statistics component instead. A sample alignment component must be placed upstream to process feature data and generate model results containing IV and CV values. |
| [FeaturePsiComponent.java](FeaturePsiComponent.md) | file | FeaturePsiComponent is a vertical federated learning component that supports binary classification scenarios and must be executed immediately after the Segment component. It checks the input dataset type and label distribution, generates task parameters, and processes the results. |
| [FeatureSelectionComponent.java](FeatureSelectionComponent.md) | file | The FeatureSelectionComponent is a feature selection component that checks whether member features are consistent, ensures the feature lists for horizontal modeling are identical, and stops task creation when no features are present. |


