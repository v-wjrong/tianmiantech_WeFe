# Basic Information

|      |      |
|------|------|
| Name | serving-service |
| Language | .java |
| Code Path | WeFe/serving/serving-service |
| Package Name | docs.serving.serving-service |
| Brief Description | Java privacy computing client module, supporting RSA/SM2 signatures, HTTP POST, and JSON, enabling anonymous query, private set intersection, and secure prediction. A core component of federated learning with microservices architecture, managing configuration, prediction, persistence, and secure communication to support system initialization, joint prediction, and service governance throughout the entire process. |

# Description

## Overview  
This module is a hybrid system integrating privacy computing and federated learning capabilities, with core responsibilities including secure data interaction (similar to an encrypted gateway mode) and distributed machine learning collaboration (similar to a master-slave architecture). The interface specification follows a layered design: the base layer employs RSA/SM2 signatures and JSON format (e.g., PirClient), while the service layer adheres to RESTful standards and the template method pattern (e.g., AbstractApi). Key data structures are aggregated into five categories: key configurations (client key pairs/SM2 keys), computation parameters (FederatedPredictParam/query parameters), system configurations (PSI batch size/service addresses), persistent models (PredictLogMySqlModel), and status enumerations (ServiceTypeEnum). External dependencies include cryptographic libraries (RSA/SM2), the Spring ecosystem (JPA/Cloud), multi-database drivers (MySQL/Doris/Hive), and HTTP components. For example, PirClient handles anonymous queries, while PromoterPredictor coordinates multi-party predictions.

## Core Business Scenarios  
The module supports end-to-end scenarios for privacy computing and federated learning, with business processes consolidated into: 1) Secure initialization (key generation → configuration loading → service registration); 2) Joint computation (feature signing → multi-party PSI → model prediction → result aggregation); 3) Governance loop (log recording → fee settlement). Typical interactions adopt a hybrid mode: privacy computing resembles an API gateway (unified signature verification), while federated learning follows a master-slave architecture (coordinated by PromoterPredictor). Functional completeness is reflected in the synergy of encrypted communication (SM2/RSA), member management (member_id), prediction engines (Predicter), and persistence (Database). For instance, in financial scenarios, MultiPsi enables inter-bank data comparison → ModelPredictClient initiates secure predictions → PredictLogMySqlModel records the process. APIs cover initialization, prediction, and scheduled tasks, with integration examples visible in the ServingService startup process (loading handlers → initializing listeners → launching API services).


### Package Internal Structure View

None

# File List

| Name   | Type  | Description |
|-------|------|-------------|
| [com](src/main/java/com/_module.md) | folder | Config Class: A Spring component that loads external configurations, defines properties such as file paths and email subjects, and supports UTF-8 encoding.  XxxModelProcessor Class: Inherits from an abstract class with empty implementations of pre-processing and post-processing methods.  Federated Learning Core API: Provides functionalities such as encrypted communication and member management, designed in a RESTful style.  Prediction Engine: Supports joint prediction, including standard, batch, and debug modes.  ORM Layer: Implements data management using JPA, containing 20+ entity classes.  Toolset: Includes signature verification, encryption, and more.  Enum Module: Defines service statuses and types.  Privacy Computing Framework: Handles PSI/PIR/SA requests.  Feature Management: Unifies the management of data sources and models.  Service Governance: Manages global configurations and model lifecycle.  Scheduled Tasks: Executes statistics and maintains status.  DTO Management: Encapsulates business data interactions.  Log Processing: Records API logs to MySQL.  Startup Listener: Executes initialization tasks.  Feature Processing Framework: Annotation and SQL-driven.  ServingService Main Class: Spring Boot application startup configuration. |


