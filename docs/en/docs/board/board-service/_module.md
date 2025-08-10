# Basic Information

|      |      |
|------|------|
| Name | board-service |
| Language | .java |
| Code Path | WeFe/board/board-service |
| Package Name | docs.board.board-service |
| Brief Description | The module system encompasses full-stack functionalities of the federated learning platform, including file system management, session state maintenance, Spring Bean configuration, data persistence, API services, scheduled tasks, exception handling, and componentized machine learning workflows. The core modules provide file lifecycle management, RESTful interfaces, JPA data operations, and distributed communication protocols, supporting both horizontal and vertical federated learning scenarios. Adopting a layered design, it integrates technologies such as Spring, gRPC, and cryptographic libraries to enable end-to-end collaborative workflows from data preprocessing to model training. |

# Description

## Overview  
This module serves as the core service matrix of the federated learning platform, integrating capabilities such as file system management, session state maintenance, Spring container configuration, data persistence, and distributed communication, akin to an enterprise-level AI collaboration hub. Unified interface standards encompass RESTful APIs (layered inheritance of AbstractApi), JPA specifications (BaseRepository extensions), and Protobuf/gRPC protocols (TransferServiceGrpc). Key data structures form a multi-dimensional system: business entity classes (JobMySqlModel), validation models (Input with @Check annotations), enumeration constants (ServiceStatus), and transmission metadata (TransferMeta sharding units). External dependencies focus on the Spring ecosystem (JPA/WebSocket), encryption components (RSA/AES), machine learning frameworks (PaddlePaddle/XGBoost), and storage systems (MySQL/LMDB). For example, DownloadDeepLearningModel handles model files, while GenerateRsaKeyPairApi manages key lifecycle.  

## Core Business Scenarios  
The module supports end-to-end federated learning scenarios: 1) Secure initialization (RSA key generation → CA certificate cache refresh → gateway connection test); 2) Collaborative modeling (data sharding and deduplication → PSI sample alignment → horizontal logistic regression training); 3) System operations (scheduled cleanup of inactive accounts → hot configuration updates → file shard uploads). Interaction modes blend synchronous CRUD (e.g., AccountService), asynchronous workflows (ModelExportService), and event-driven mechanisms (ApplicationListener), resembling a hybrid of a workflow engine and message bus. Typical applications include cross-institution data fusion (Bloom filter deduplication), flowchart node management (BaseFlowGraph for cyclic dependency prevention), and real-time communication (WebSocket duplex sessions). Functional completeness is reflected in multi-component coordination, such as project deletion triggering cascaded cleanup and model exports synchronously pushing keys to the Serving system.


### Package Internal Structure View

None

# File List

| Name   | Type  | Description |
|-------|------|-------------|
| [com](src/main/java/com/_module.md) | folder | The module system encompasses the full-stack functionality of the federated learning platform, including file system management, session state maintenance, Spring Bean configuration, data persistence, API services, scheduled tasks, exception handling, and componentized machine learning workflows. The core modules provide file lifecycle management, RESTful interfaces, JPA data operations, and distributed communication protocols, supporting both horizontal and vertical federated learning scenarios. Adopting a layered design, it integrates technologies such as Spring, gRPC, and cryptographic libraries to enable end-to-end collaborative workflows from data preprocessing to model training. |


