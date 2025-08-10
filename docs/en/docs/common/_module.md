# Basic Information

|      |      |
|------|------|
| Name | common |
| Language | .java |
| Code Path | WeFe/common |
| Package Name | docs.common |
| Brief Description | Java basic utility library, including configuration management, data processing, validation, HTTP communication, etc., with dependencies such as Log4j. Full-stack web application solution, supporting API management, access control, logging, with dependencies such as Spring. JPA data access layer, providing CRUD and dynamic queries, dependent on JPA. Cross-cloud data storage, supporting sharding and connection pool management, dependent on Druid. Protobuf protocol, supporting data serialization. MongoDB data management, supporting CRUD and aggregation queries. Federated learning framework, including health checks, configuration management, etc. CAPTCHA service, supporting SMS/email delivery. Cryptography toolkit, supporting key management and certificate operations. JDBC framework, supporting multi-database operations. |

# Description

## Overview  
This module serves as the full-stack infrastructure for the federated learning platform, with core responsibilities including data governance (multi-database CRUD/dynamic queries), secure communication (national cryptographic algorithms/certificate management), and development support (configuration management/captcha services). The interface specification follows a layered design, such as the AbstractApi base class system, JdbcScanner abstract queries, and factory patterns (ClientFactory). Key data structures encompass pagination objects (Pageable), certificate models (CryptoKeyPair), condition builders (Where), and captcha enums (CaptchaSendChannel). External dependencies include the Spring framework, BouncyCastle, MongoDB drivers, and cloud platform SDKs, such as Log4j for logging and Alibaba Cloud SMS SDK for captcha delivery.  

The module adopts a multi-mode integrated design, resembling a middleware collection. For example, Configurations manages multi-environment settings, JdbcClient standardizes JDBC operations, and CertService handles certificate issuance. Technical features include annotation-driven mechanisms (@FlowLimitByMobile), strategy enums (ServiceType), and stream processing (BatchConsumer). Typical implementations involve SM2 key generation → PEM-format storage or dynamic query construction via Where.equal().groupBy().  

## Core Business Scenarios  
The module supports three key closed loops: 1) **Security Loop**, involving captcha services (SMS/email) → certificate management (SM2 signatures) → HTTPS communication, such as SMS captcha validation during user registration; 2) **Data Loop**, combining JdbcScanner stream queries → MongoDB aggregation → paginated storage, akin to an ETL pipeline; 3) **Service Loop**, spanning health checks (UnionService detection) → API execution (reflective invocation) → audit logging.  

A unified interaction model combines chained calls with factory patterns. For instance, the Where builder generates dynamic SQL conditions, while ClientFactory selects captcha clients by channel. Functional completeness is reflected in coverage of national cryptographic algorithms (SM3WITHSM2), multi-database support (MySQL/MongoDB), and full lifecycle management (e.g., certificate WAIT_VERIFY→VALID). Typical applications include federated learning task configuration (resource selectors), high-concurrency data sharding (PageInputModel), and cross-cloud storage switching (OSS credential management). Examples include HttpRequest auto-handling 302 redirects and Validator verifying ID card formats.


### Package Internal Structure View

None

# File List

| Name   | Type  | Description |
|-------|------|-------------|
| [java](java/common-data-mysql/src/main/java/com/_module.md) | module | Java basic utility library, including configuration management, data processing, validation, HTTP communication, etc., with dependencies such as Log4j. Full-stack web application solution, supporting API management, access control, logging, with dependencies such as Spring. JPA data access layer, providing CRUD and dynamic queries, dependent on JPA. Cross-cloud data storage, supporting sharding and connection pool management, dependent on Druid. Protobuf protocol, supporting data serialization. MongoDB data management, supporting CRUD and aggregation queries. Federated learning framework, including health checks, configuration management, etc. CAPTCHA service, supporting SMS/email delivery. Cryptography toolkit, supporting key management and certificate operations. JDBC framework, supporting multi-database operations. |


