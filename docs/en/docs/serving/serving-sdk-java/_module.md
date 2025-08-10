# Basic Information

|      |      |
|------|------|
| Name | serving-sdk-java |
| Language | .java |
| Code Path | WeFe/serving/serving-sdk-java |
| Package Name | docs.serving.serving-sdk-java |
| Brief Description | This module provides a federated learning prediction framework, supporting logistic regression and XGBoost algorithms, covering single/batch processing, parameter validation, and result merging. It defines standardized processes through abstract classes and template methods, leveraging annotations and reflection for dynamic loading. Key components include model processors, algorithm managers, and thread pools, suitable for both real-time and offline prediction scenarios. |

# Description

## Overview  
This module is a standardized prediction framework in federated learning environments, with its core responsibility being the unified management of the entire model prediction process (single/batch processing, parameter validation, result conversion) and multi-party result merging. It employs template method patterns through abstract base classes (e.g., AbstractAlgorithm/AbstractBatchModelProcessor), with key data structures including BaseModel, PredictParams, feature mapping, and prediction result models (e.g., LrPredictResultModel). External dependencies involve the XGBoost framework, JObject, multi-threading utilities (e.g., CountDownLatch), and federated learning components (e.g., WeFe). For instance, EmptyModelProcessor provides placeholder implementations, while AlgorithmManager dynamically loads algorithm instances via reflection.

## Key Business Scenarios  
The module supports horizontal/vertical federated prediction, with a typical workflow: parameter initialization → local computation → multi-party result merging → desensitized output, resembling a hybrid of MapReduce and distributed decision engines. The interaction model adopts a Promoter-Provider architecture, dynamically assembling components via annotations (e.g., @ModelProcessor) and factory patterns (e.g., AlgorithmManager). Functional completeness is demonstrated through support for logistic regression (scorecard binning), XGBoost (tree structure merging), and exception handling (StateCode status codes). Examples include XgboostVertPromoterAlgorithm merging remote tree structures in financial risk control or standardizing feature queries via the PredictBehavior interface. APIs cover single/batch prediction, encryption configuration management, and thread pool task scheduling.


### Package Internal Structure View

None

# File List

| Name   | Type  | Description |
|-------|------|-------------|
| [com](src/main/java/com/_module.md) | folder | This module provides a federated learning prediction framework, supporting logistic regression and XGBoost algorithms, covering single/batch processing, parameter validation, and result merging. It defines standardized processes through abstract classes and template methods, leveraging annotations and reflection for dynamic loading. Key components include model processors, algorithm managers, and thread pools, suitable for both real-time and offline prediction scenarios. |


