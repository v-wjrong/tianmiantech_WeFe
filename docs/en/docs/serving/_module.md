# Basic Information

|      |      |
|------|------|
| Name | serving |
| Language | .java |
| Code Path | WeFe/serving |
| Package Name | docs.serving |
| Brief Description | The federated learning prediction framework uniformly manages the prediction process and result merging, supporting horizontal/vertical federated learning, and relies on XGBoost and multi-threading tools. The privacy-preserving computing system integrates secure data interaction and collaborative machine learning, adopts a layered design, supports encrypted communication and joint computation, and depends on encryption libraries and the Spring ecosystem. |

# Description

## Overview  
This module is a collaborative system integrating federated learning and privacy-preserving computation, with core responsibilities including secure data interaction (similar to an encrypted gateway) and distributed prediction process management (similar to a master-slave architecture). Standardization is achieved through layered interface design (base layer RSA/SM2 signatures and service layer RESTful APIs) and the template method pattern (e.g., AbstractAlgorithm/AbstractApi). Key data structures comprise five categories: key configurations (SM2 key pairs), computation parameters (FederatedPredictParam), model objects (LrPredictResultModel), system configurations (PSI batch size), and status enumerations (ServiceTypeEnum). External dependencies involve cryptographic libraries (SM2/RSA), machine learning frameworks (XGBoost), multi-database drivers (MySQL/Doris), and federated components (WeFe). For instance, PirClient handles anonymous queries, while AlgorithmManager dynamically loads prediction algorithms.

## Core Business Scenarios  
The module supports end-to-end federated prediction and privacy-preserving computation, with typical workflows including: 1) Secure initialization (key generation → service registration); 2) Joint computation (PSI alignment → model prediction → result aggregation); 3) Governance loop (log recording → fee settlement). The interaction model combines an API gateway (unified signature verification) with a master-slave architecture (PromoterPredictor coordination). Functional completeness is reflected in encrypted communication (SM2), multi-algorithm support (XGBoost tree merging/logistic regression binning), and state management (StateCode). For example, in financial scenarios, MultiPsi performs bank data comparison → XgboostVertPromoterAlgorithm merges remote prediction results → PredictLogMySqlModel records the process. APIs cover initialization, batch prediction, and scheduled tasks, with integration examples visible in the ServingService startup process (loading handlers → listener initialization → API service exposure).


### Package Internal Structure View

None

# File List

| Name   | Type  | Description |
|-------|------|-------------|
| [serving-sdk-java](serving-sdk-java/src/main/java/com/_module.md) | module | This module provides a federated learning prediction framework, supporting logistic regression and XGBoost algorithms, covering single/batch processing, parameter validation, and result merging. It defines standardized processes through abstract classes and template methods, leveraging annotations and reflection for dynamic loading. Key components include model processors, algorithm managers, and thread pools, suitable for both real-time and offline prediction scenarios. |
| [serving-service](serving-service/src/main/java/com/_module.md) | module | Java privacy computing client module, supporting RSA/SM2 signatures, HTTP POST, and JSON, enabling anonymous query, private set intersection, and secure prediction. A core component of federated learning with microservices architecture, managing configuration, prediction, persistence, and secure communication to support system initialization, joint prediction, and service governance throughout the entire process. |


