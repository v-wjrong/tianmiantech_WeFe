# Basic Information

|      |      |
|------|------|
| Name | fusion |
| Language | .java |
| Code Path | WeFe/fusion |
| Package Name | docs.fusion |
| Brief Description | The core management system of federated learning integrates data persistence, privacy-preserving computation (PSI algorithm), and task scheduling, supporting full lifecycle management. It adopts a layered architecture, relying on Spring Data JPA and multiple database drivers. Typical workflows include initialization, data preparation, secure computation, and result callback. |

# Description

## Overview  
This module serves as the core management system of the federated learning platform, adopting a layered architecture design that integrates system control, data management, task scheduling, and privacy computing functionalities. Key responsibilities include: 1) achieving data persistence through a hierarchical storage system (e.g., MySQL/MergeTree); 2) ensuring secure cross-institution data alignment via the PSI (Private Set Intersection) algorithm; 3) providing a full lifecycle management toolkit (e.g., Bloom filters/primary key generation). The interface specification uniformly employs JPA annotations and RESTful style, such as deriving various APIs from the `AbstractApi` base class and implementing extended queries with `@Query`. Critical data structures encompass paginated result sets, encrypted business entities (e.g., `GlobalConfigMysqlModel`), and PSI execution parameters (e/n/d). External dependencies include Spring Data JPA, RSA encryption components, connection pool management (e.g., HikariCP), and multiple database drivers (MySQL/Hive/Impala).  

The module also implements dual-end logic for the Privacy-Preserving Set Intersection (PSI) protocol and federated learning support components. Core responsibilities include secure data alignment (similar to blind signature processes), Bloom filter operations, and task state management. Interface specifications cover abstract base classes for Server/Client, enum definitions, and DTO transmission models, such as `dataTransform` for data conversion and `generateBlindingFactor` for metadata download. Key data structures include `BigInteger` encryption parameters, `BitSet` bit collections, `BloomFilterDto` transmission objects, and enums like `PSIActuatorRole`. External dependencies involve the JObject serialization framework, RSA-PSI algorithms, and Java cryptography components. For instance, `ActuatorCache` manages executor mappings, while `BloomFilterUtils` simplifies I/O operations.  

## Key Business Scenarios  
The module supports end-to-end federated learning process management, with a typical workflow as follows: 1) system initialization (generating RSA keys/validating `memberName`); 2) data preparation (`DatasetApi` managing CSV/Excel parsing); 3) secure computation (`PsiClientActuator` executing encrypted sharding); 4) result callback (`TaskResultManager` dynamically creating tables for storage). The interaction model combines producer-consumer patterns (batch processing 10,000 rows of data) and state machine-driven operations (`TaskStatus` managing 7 states). Functional completeness is reflected in: encrypted validation (≤5 field combinations), thread-safe operations (`ConcurrentHashMap` for task management), and exception handling chains (`StatusCodeWithException`). Integration cases span from basic configurations (`DataSourceConfig` for multi-data sources) to complex business scenarios (RSA-PSI algorithm switching), resembling a distributed ETL console.  

Typical processes also follow the sequence: Client initialization → metadata exchange → bucket encryption → Server matching → result transmission, employing multi-threaded paginated processing akin to MapReduce. Full functionality covers data preprocessing (e.g., `parseAndMatch`), cryptographic transformations (RSA/DH algorithms), state coordination (`FusionTaskStatus` enum), and filter persistence (`writeTo`/`readFrom`). Interaction modes are role-based (server/client) and state-driven (e.g., `Progress.Ready` triggering execution), with API types including basic operations (add/contains), cryptographic functions (`generateKeys`), and thread pool task submissions. For example, MD5 hashing ensures data consistency, `AlgorithmType.DH` supports key exchange, and DTO patterns enable cross-node transmission.


### Package Internal Structure View

None

# File List

| Name   | Type  | Description |
|-------|------|-------------|
| [fusion-core](fusion-core/src/main/java/com/_module.md) | module | The module implements the Privacy-Preserving Set Intersection (PSI) protocol, including Server/Client base classes, data conversion, and metadata processing, relying on the RSA-PSI algorithm and JObject serialization. The Bloom filter module supports efficient operations and persistence, integrating cryptographic tools and thread pool management. The enumeration module defines key federated learning dimensions such as task status and algorithm types. The DTO module encapsulates Bloom filters and metadata, enabling serialized transmission of PSI protocol components. |
| [fusion-service](fusion-service/src/main/java/com/_module.md) | module | The core system of the federated learning platform includes control, data, and task modules, supporting the entire workflow of initialization, data management, and task scheduling. It features a layered architecture design, unified interface standards, and integrates key data structures with multiple service components. |


