# Basic Information

|      |      |
|------|------|
| Name | fusion-service |
| Language | .java |
| Code Path | WeFe/fusion/fusion-service |
| Package Name | docs.fusion.fusion-service |
| Brief Description | The core system of the federated learning platform includes control, data, and task modules, supporting the entire workflow of initialization, data management, and task scheduling. It features a layered architecture design, unified interface standards, and integrates key data structures with multiple service components. |

# Description

## Overview  
This module serves as the core management system of the federated learning platform, adopting a layered architecture design that integrates system control, data management, task scheduling, and privacy computing functionalities. Its core responsibilities include: 1) achieving data persistence through a hierarchical storage system (MySQL/MergeTree); 2) ensuring secure cross-institution data alignment based on the PSI (Private Set Intersection) algorithm; 3) providing a full lifecycle management toolkit (Bloom filters/primary key generation, etc.). The interface specifications uniformly employ JPA annotations and RESTful style, such as deriving various APIs from the AbstractApi base class and implementing extended queries via @Query. Key data structures encompass paginated result sets, encrypted business entities (e.g., GlobalConfigMysqlModel), and PSI execution parameters (e/N/d). External dependencies include Spring Data JPA, RSA encryption components, connection pool management (e.g., HikariCP), and multiple database drivers (MySQL/Hive/Impala).

## Primary Business Scenarios  
The module supports end-to-end federated learning process management, with a typical workflow as follows: 1) system initialization (generating RSA keys/validating memberName); 2) data preparation (DatasetApi managing CSV/Excel parsing); 3) secure computation (PsiClientActuator executing encrypted sharding); 4) result callback (TaskResultManager dynamically creating tables for storage). The interaction model combines the producer-consumer pattern (batch processing 10,000 rows of data) with state machine-driven operations (TaskStatus managing 7 states). Functional completeness is reflected in: encrypted validation (≤5 field combinations), thread-safe operations (ConcurrentHashMap managing tasks), and exception handling chains (StatusCodeWithException). Integration cases span from basic configurations (DataSourceConfig multi-data sources) to complex business scenarios (RSA-PSI algorithm switching), resembling a distributed ETL console.


### Package Internal Structure View

None

# File List

| Name   | Type  | Description |
|-------|------|-------------|
| [com](src/main/java/com/_module.md) | folder | The core system of the federated learning platform includes control, data, and task modules, supporting the entire workflow from initialization to data management and task scheduling. It features a layered architecture design, unified interface standards, and integrates key data structures with multiple service components. |


