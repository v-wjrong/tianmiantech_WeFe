# Basic Information

|      |      |
|------|------|
| Name | repository |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/database/repository |
| Package Name | docs.board.board-service.src.main.java.com.welab.wefe.board.service.database.repository |
| Brief Description | The resource management repository layer implemented by Spring Data JPA uniformly manages various data resources and provides CRUD extension functionalities. It covers business scenarios such as data cleanup, status maintenance, and usage statistics, while supporting native SQL and transactional operations. |

# Description

## Overview  
This module is a generic data access layer built on Spring Data JPA, with its core responsibility being the unified management of persistence operations for various business entities (such as datasets, tasks, messages, etc.), akin to an enterprise-level data mid-platform architecture. The interface specifications adhere to the JPA standard, extending basic CRUD capabilities through the BaseRepository base class, and supporting features like native SQL queries (e.g., countByName for counting records with the same name), batch updates, and pagination conversion. Key data structures include 40+ MySqlModel entity classes (e.g., TaskMySqlModel, MessageMysqlModel, etc.), all utilizing String-type primary keys. External dependencies are limited to the Spring Data JPA framework, with @Transactional and @Modifying ensuring transaction safety. For example, ProjectDataSetRepository automatically clears the persistence context when performing batch updates to dataset states.

## Key Business Scenarios  
The module supports full business lifecycle management, adopting a repository pattern for unified interaction, similar to a resource management center design. Typical workflows include: data preprocessing (ImageDataSetSampleRepository managing annotated samples), task scheduling (JobRepository tracking runtime status), message processing (MessageQueueRepository maintaining message queues), and access control (AccountRepository managing user states). Interaction modes are exposed via JPA interfaces, such as ProjectFlowRepository providing pin/unpin operations for workflows, and MemberChatRepository implementing message state updates. API types encompass basic CRUD (90%), custom queries (e.g., listAllTags), and business operations (e.g., disableDataSetWhenMemberExist). Integration examples include transactional deletion (ChatUnreadMessageRepository) and multi-condition retrieval (TaskRepository.findTaskWithGridSearch).


### Package Internal Structure View

```mermaid
graph TD
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
```

This flowchart illustrates the database repository structure within a Java project, comprising three subdirectories (data_resource, fusion, and base) along with numerous Java files directly under the repository directory. Each subdirectory contains its respective implementation classes, presenting a multi-level tree structure that reflects the modular design of the project's data access layer.

# File List

| Name   | Type  | Description |
|-------|------|-------------|
| [TaskProgressRepository.java](TaskProgressRepository.md) | file | Task progress repository interface, inherits from the base repository, operates on the task progress MySQL model, with the primary key type as string. |
| [DataSourceRepository.java](DataSourceRepository.md) | file | This is a Spring Data JPA repository interface that extends the base repository and defines a native SQL query method for counting data sources by name. |
| [ChatLastAccountRepository.java](ChatLastAccountRepository.md) | file | This is a Spring Repository interface for operating on ChatLastAccountMysqlModel data, providing methods to delete records by accountId and liaisonAccountId. |
| [ChatUnreadMessageRepository.java](ChatUnreadMessageRepository.md) | file | The ChatUnreadMessageRepository interface extends BaseRepository, providing methods to query unread messages and delete records based on sender and recipient accounts. |
| [DataSetColumnRepository.java](DataSetColumnRepository.md) | file | This is a Spring Data JPA repository interface designed for operating dataset series models. It extends the base repository and defines a delete method that removes records based on dataset ID, supporting transactions and automatic cache clearance. |
| [ModelOotRecordRepository.java](ModelOotRecordRepository.md) | file | This is a Spring Repository interface, extending from BaseRepository, used for operating the ModelOotRecordMysqlModel entity class with a primary key type of String. |
| [OperationLogRepository.java](OperationLogRepository.md) | file | Operation log repository interface, inherits from the base repository class, with the operation log model being of MySQL type and the primary key as a string. |
| [JobMemberRepository.java](JobMemberRepository.md) | file | The JobMemberRepository interface extends BaseRepository, operates on the JobMemberMySqlModel entity, with the primary key type being String. |
| [GlobalConfigRepository.java](GlobalConfigRepository.md) | file | This is a Spring Repository interface that extends BaseRepository, designed for operating on GlobalConfigMysqlModel data and providing query functionality by the group field. |
| [ProjectMemberAuditRepository.java](ProjectMemberAuditRepository.md) | file | Project members review repository interface, inheriting the base repository, providing the functionality to delete specified member review records, including both their reviewed and being-reviewed records, implemented via native SQL. |
| [DataOutputInfoRepository.java](DataOutputInfoRepository.md) | file | Data Output Information Repository Interface, inherits from the base repository class, operates on the data output information MySQL model, with the primary key type as string. |
| [OutputModelRepository.java](OutputModelRepository.md) | file | This is a Spring Data JPA repository interface that extends the base repository class, used for operating on the OutputModelMysqlModel entity with a primary key type of String. |
| [PartnerConfigRepository.java](PartnerConfigRepository.md) | file | The PartnerConfigRepository interface extends BaseRepository and provides a method to query PartnerConfigMysqlModel by memberId. |
| [TaskRepository.java](TaskRepository.md) | file | The TaskRepository interface extends BaseRepository and includes two native SQL query methods: findOne retrieves the latest task by jobId, flowNodeId, and role; findTaskWithGridSearch searches for a list of tasks requiring grid search under non-arbiter roles. |
| [CertInfoRepository.java](CertInfoRepository.md) | file | The CertInfoRepository interface defines two methods: updateStatus updates the status based on ID, and resetCert resets the status of all certificates. Both use native SQL and support transactions. |
| [FeatureJobMemberRepository.java](FeatureJobMemberRepository.md) | file | This is a Spring repository interface that extends the base repository class, designed to manage JobMemberMySqlModel type data with a primary key of String type. |
| [MemberChatRepository.java](MemberChatRepository.md) | file | Member Chat Repository Interface, including methods for querying chat history between both parties, retrieving chat lists, and updating message status. |
| [FlowActionLogRepository.java](FlowActionLogRepository.md) | file | This is a Spring repository interface that extends the base repository class, designed for operating on FlowActionLogMySqlModel type data with String as the primary key. |
| [BlacklistRepository.java](BlacklistRepository.md) | file | This is a Spring Data JPA repository interface that extends the base repository class and provides methods for querying blacklist data by member ID. |
| [FlowTemplateRepository.java](FlowTemplateRepository.md) | file | This is a Spring repository interface that extends the base repository class, used for operating on FlowTemplateMySqlModel data with a primary key type of String. |
| [MessageRepository.java](MessageRepository.md) | file | The MessageRepository interface defines two methods: completeApplyDataResourceTodo updates the to-do status of a specified project and data resource to completed and read; completeApplyJoinProjectTodo updates the to-do status of joining a project for a specified association ID to completed and read. Both use native SQL and support transactions. |
| [CertKeyInfoRepository.java](CertKeyInfoRepository.md) | file | This is a Spring JPA repository interface that extends the base repository class, designed for operating on the CertKeyInfoMysqlModel data model with a primary key type of String. |
| [AccountRepository.java](AccountRepository.md) | file | The AccountRepository interface provides account management functionalities, including querying by mobile number, revoking administrator privileges, updating the last operation time, disabling accounts inactive for 90 days, deleting accounts inactive for 180 days, and updating UI configurations. |
| [TrackingMetricRepository.java](TrackingMetricRepository.md) | file | This is a Spring framework repository interface, extending the base repository class, designed for operating on the TrackingMetricMysqlModel data model with a primary key type of String. |
| [ImageDataSetSampleRepository.java](ImageDataSetSampleRepository.md) | file | The ImageDataSetSampleRepository interface extends BaseRepository, providing methods for deletion, querying label lists, and counting sample quantities, with support for dataset ID operations. |
| [ProjectFlowNodeRepository.java](ProjectFlowNodeRepository.md) | file | Project Process Node Repository Interface, providing methods to query nodes by process ID and node ID, as well as the functionality to delete nodes in a specified process that are not included in a given node ID list. |
| [ProjectMemberRepository.java](ProjectMemberRepository.md) | file | Project member repository interface, inherits from the base repository, defines query methods to retrieve all collaborator member IDs. |
| [ProjectDataSetRepository.java](ProjectDataSetRepository.md) | file | ProjectDataSetRepository interface definition: 1. Disable datasets when members exit; 2. Query available datasets in a project; 3. Count the number of datasets pending review. |
| [FlowActionQueueRepository.java](FlowActionQueueRepository.md) | file | This is a Spring framework repository interface, extending the base repository class, for operating on FlowActionQueueMySqlModel type data with String as the primary key type. |
| [MessageQueueRepository.java](MessageQueueRepository.md) | file | Message queue repository interface, inherits from the base repository, operates on the message queue MySQL model, with the primary key type as string. |
| [TaskContextRepository.java](TaskContextRepository.md) | file | This is a Spring Repository interface, extending from BaseRepository, designed for manipulating data of type TaskContextMySqlModel with a primary key of type String. |
| [JobRepository.java](JobRepository.md) | file | The JobRepository interface extends BaseRepository and provides three native SQL query methods: finding tasks by jobId and role, finding the latest task by flowId and role, and counting the number of unfinished tasks. |
| [CertRequestInfoRepository.java](CertRequestInfoRepository.md) | file | The interface CertRequestInfoRepository extends BaseRepository and is used to operate CertRequestInfoMysqlModel data, with the primary key type being String. |
| [RoleCountsRepository.java](RoleCountsRepository.md) | file | The interface RoleCountsRepository is defined, with no specific methods. |
| [TaskResultRepository.java](TaskResultRepository.md) | file | This is a Spring TaskResultRepository interface, extending BaseRepository, used for manipulating TaskResultMySqlModel type data with a primary key of String type. |
| [VerificationCodeRepository.java](VerificationCodeRepository.md) | file | This is a Spring Repository interface, extending from BaseRepository, used for manipulating data of type VerificationCodeMysqlModel with a primary key type of String. |
| [ProjectFlowRepository.java](ProjectFlowRepository.md) | file | The ProjectFlowRepository interface provides project flow status statistics, pinning, and unpinning functionalities, utilizing native SQL queries and update operations. |
| [ProjectRepository.java](ProjectRepository.md) | file | The ProjectRepository interface includes functionalities for querying projects created by non-administrators more than 10 days ago, retrieving the last startup time of projects, querying projects by name or ID, as well as pinning and unpinning features. |
| [base](base/_module.md) | package | BaseRepositoryFactoryBean defines a generic factory bean that extends the JPA repository creation process. RepositoryManager caches the model-repository mapping and supports both scanning and manual registration. BaseRepositoryImpl implements common JPA operations, including querying, updating, pagination, and SQL functionalities. The BaseRepository interface extends standard JPA capabilities, supporting field-based queries, updates, and transaction handling. |
| [fusion](fusion/_module.md) | package | Multiple Spring Data repository interfaces are defined, all extending BaseRepository, operating on different entity classes with String as the primary key. They include CRUD operations and specific query methods, such as querying the latest record by business ID or deleting records by ID. |
| [data_resource](data_resource/_module.md) | package | Spring repository interface definitions: BloomFilterRepository operates on the Bloom filter model; DataResourceUploadTaskRepository manages upload tasks, including cleanup and timeout handling; DataResourceRepository provides methods for tag queries, counting, and updates; TableDataSetRepository and ImageDataSetRepository operate on table data and image data models respectively. |


