# Basic Information

|      |      |
|------|------|
| Name | database |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/database |
| Package Name | docs.board.board-service.src.main.java.com.welab.wefe.board.service.database |
| Brief Description | A generic data access layer based on Spring Data JPA, uniformly managing business entity persistence with support for CRUD, batch updates, and pagination. Key data structures include 40+ entity classes, relying on Spring Data JPA to ensure transactional safety. It supports full business lifecycle management, covering scenarios such as data preprocessing and task scheduling. |

# Description

## Overview  
This module serves as the core data persistence layer of the federated learning platform, built on Spring Data JPA and adopting an enterprise-level data mid-platform architecture to uniformly manage multi-domain business entities (e.g., datasets, tasks, certificates, etc.). The interface specifications comply with JPA standards, extending CRUD capabilities through BaseRepository while supporting native SQL queries, batch updates, and pagination conversion (e.g., `countByName` for counting records with the same name). Key data structures form three major systems: certificate management (e.g., `CertKeyInfoMysqlModel`), federated learning (e.g., `JobMySqlModel`), and data resources (e.g., `TableDataSetMysqlModel`), all utilizing String-type primary keys. External dependencies focus on MySQL, Spring Data JPA, and encryption components (e.g., `DatabaseEncryptConverter`), with transaction safety ensured via `@Transactional`. For instance, `GlobalConfigMysqlModel` implements encrypted storage for configuration items, while `ProjectDataSetRepository` supports batch updates of dataset statuses.  

## Key Business Scenarios  
The module supports the entire federated learning lifecycle and collaboration with peripheral systems, functioning similarly to a workflow engine combined with a message bus. Typical scenarios include: data preprocessing (`ImageDataSetSampleRepository` managing annotated samples), task scheduling (`JobRepository` monitoring progress), certificate issuance (CA audit → key storage), and message processing (`MessageQueueRepository` maintaining pending tasks). Interaction modes span three dimensions: resource-oriented (managing annotated data), task-oriented (tracking process nodes), and message-oriented (handling status updates), with operations exposed via JPA interfaces (e.g., `ProjectFlowRepository` providing workflow pinning functionality). API types encompass basic CRUD (90%), custom queries (e.g., `listAllTags`), and business operations (e.g., `disableDataSetWhenMemberExist`). Integration examples include transactional deletion (`ChatUnreadMessageRepository`) and multi-condition retrieval (`TaskRepository.findTaskWithGridSearch`).


### Package Internal Structure View

```mermaid
graph TD
    database --> repository
    database --> entity
    database --> DataSourceConfig.java
    repository --> data_resource
    repository --> fusion
    repository --> base
    repository --> TaskProgressRepository.java
    repository --> DataSourceRepository.java
    repository --> ChatLastAccountRepository.java
    repository --> ChatUnreadMessageRepository.java
    repository --> DataSetColumnRepository.java
    repository --> ModelOotRecordRepository.java
    repository --> OperationLogRepository.java
    repository --> JobMemberRepository.java
    repository --> GlobalConfigRepository.java
    repository --> ProjectMemberAuditRepository.java
    repository --> DataOutputInfoRepository.java
    repository --> OutputModelRepository.java
    repository --> PartnerConfigRepository.java
    repository --> TaskRepository.java
    repository --> CertInfoRepository.java
    repository --> FeatureJobMemberRepository.java
    repository --> MemberChatRepository.java
    repository --> FlowActionLogRepository.java
    repository --> BlacklistRepository.java
    repository --> FlowTemplateRepository.java
    repository --> MessageRepository.java
    repository --> CertKeyInfoRepository.java
    repository --> AccountRepository.java
    repository --> TrackingMetricRepository.java
    repository --> ImageDataSetSampleRepository.java
    repository --> ProjectFlowNodeRepository.java
    repository --> ProjectMemberRepository.java
    repository --> ProjectDataSetRepository.java
    repository --> FlowActionQueueRepository.java
    repository --> MessageQueueRepository.java
    repository --> TaskContextRepository.java
    repository --> JobRepository.java
    repository --> CertRequestInfoRepository.java
    repository --> RoleCountsRepository.java
    repository --> TaskResultRepository.java
    repository --> VerificationCodeRepository.java
    repository --> ProjectFlowRepository.java
    repository --> ProjectRepository.java
    data_resource --> BloomFilterRepository.java
    data_resource --> DataResourceUploadTaskRepository.java
    data_resource --> DataResourceRepository.java
    data_resource --> TableDataSetRepository.java
    data_resource --> ImageDataSetRepository.java
    fusion --> ExportProgressRepository.java
    fusion --> FieldInfoRepository.java
    fusion --> FusionActuatorInfoRepository.java
    fusion --> BloomFilterTaskRepository.java
    fusion --> FusionResultRepository.java
    fusion --> FusionTaskRepository.java
    fusion --> BloomFilterColumnRepository.java
    base --> BaseRepositoryFactoryBean.java
    base --> RepositoryManager.java
    base --> BaseRepositoryImpl.java
    base --> BaseRepository.java
    entity --> cert
    entity --> data_resource
    entity --> job
    entity --> chat
    entity --> data_set
    entity --> flow
    entity --> fusion
    entity --> base
    entity --> MessageMysqlModel.java
    entity --> PartnerConfigMysqlModel.java
    entity --> OutputModelMysqlModel.java
    entity --> GlobalConfigMysqlModel.java
    entity --> BlacklistMysqlModel.java
    entity --> OperationLogMysqlModel.java
    entity --> VerificationCodeMysqlModel.java
    entity --> DataSourceMysqlModel.java
    entity --> TrackingMetricMysqlModel.java
    entity --> AccountMysqlModel.java
    entity --> DataOutputInfoMysqlModel.java
    cert --> CertKeyInfoMysqlModel.java
    cert --> CertRequestInfoMysqlModel.java
    cert --> CertInfoMysqlModel.java
    data_resource --> DataResourceUploadTaskMysqlModel.java
    data_resource --> BloomFilterMysqlModel.java
    data_resource --> TableDataSetMysqlModel.java
    data_resource --> DataResourceMysqlModel.java
    data_resource --> ImageDataSetMysqlModel.java
    job --> ModelOotRecordMysqlModel.java
    job --> TaskMySqlModel.java
    job --> JobMemberMySqlModel.java
    job --> TaskResultMySqlModel.java
    job --> ProjectMemberAuditMySqlModel.java
    job --> JobMySqlModel.java
    job --> ProjectFlowNodeMySqlModel.java
    job --> ProjectFlowMySqlModel.java
    job --> ProjectDataSetMySqlModel.java
    job --> TaskProgressMysqlModel.java
    job --> TaskContextMySqlModel.java
    job --> ProjectMySqlModel.java
    job --> ProjectMemberMySqlModel.java
    chat --> ChatUnreadMessageMySqlModel.java
    chat --> MemberChatMySqlModel.java
    chat --> ChatLastAccountMysqlModel.java
    chat --> MessageQueueMySqlModel.java
    data_set --> ImageDataSetSampleMysqlModel.java
    data_set --> DataSetColumnMysqlModel.java
    flow --> FlowActionLogMySqlModel.java
    flow --> FlowTemplateMySqlModel.java
    flow --> FlowActionQueueMySqlModel.java
    fusion --> bloomfilter
    fusion --> FusionActuatorInfoMySqlModel.java
    fusion --> FusionTaskMySqlModel.java
    fusion --> FusionResultMySqlModel.java
    fusion --> FieldInfoMySqlModel.java
    fusion --> ExportProgressMySqlModel.java
    bloomfilter --> BloomFilterTaskMysqlModel.java
    bloomfilter --> BloomFilterColumnMysqlModel.java
    base --> AbstractBaseMySqlModel.java
    base --> AbstractMySqlModel.java
```

This flowchart illustrates the database-related code structure of the board-service module in the WeFe project, primarily divided into two main branches: repository (data access layer) and entity (entity classes). The repository branch contains multiple subdirectories and direct files, such as data_resource and fusion, while the entity branch is organized by business domains like cert, job, and chat. The entire structure is clearly hierarchical, fully presenting the organization of database-related code.

# File List

| Name   | Type  | Description |
|-------|------|-------------|
| [entity](entity/_module.md) | package | The module manages the entire lifecycle of digital certificates, including key storage and application issuance. The data structure includes entities such as CertKeyInfoMysqlModel and relies on the JPA framework. It supports scenarios like consortium blockchain network access authentication. |
| [DataSourceConfig.java](DataSourceConfig.md) | file | The configuration class DataSourceConfig extends AbstractJpaConfig, defining the primary data source "board" and JPA-related Beans, including the entity manager factory and transaction manager, while setting the naming strategy. |
| [repository](repository/_module.md) | package | The resource management repository layer implemented by Spring Data JPA uniformly manages various data resources and provides CRUD extension functionalities. It covers business scenarios such as data cleanup, status maintenance, and usage statistics, while supporting native SQL and transactional operations. |


