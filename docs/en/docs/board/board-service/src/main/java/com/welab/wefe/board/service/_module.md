# Basic Information

|      |      |
|------|------|
| Name | service |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service |
| Package Name | docs.board.board-service.src.main.java.com.welab.wefe.board.service |
| Brief Description | The module system encompasses full-stack functionalities of the federated learning platform, including file system management, session state maintenance, Spring Bean configuration, data persistence, API services, scheduled tasks, exception handling, and modularized machine learning workflows. The core modules provide file lifecycle management, RESTful interfaces, JPA data operations, and distributed communication protocols, supporting both horizontal and vertical federated learning scenarios. Adopting a layered design, it integrates technologies such as Spring, gRPC, and cryptographic libraries to enable end-to-end collaborative workflows from data preprocessing to model training. |

# Description

## Overview  
This module serves as the core service matrix of the federated learning platform, integrating capabilities such as file system management, session state maintenance, Spring container configuration, data persistence, and distributed communication, akin to an enterprise-level AI collaboration hub. Unified interface standards encompass RESTful APIs (layered inheritance of AbstractApi), JPA specifications (BaseRepository extensions), and Protobuf/gRPC protocols (TransferServiceGrpc). Key data structures form a multi-dimensional system: business entity classes (JobMySqlModel), validation models (Input annotated with @Check), enumerated constants (ServiceStatus), and transmission metadata (TransferMeta sharding units). External dependencies focus on the Spring ecosystem (JPA/WebSocket), cryptographic components (RSA/AES), machine learning frameworks (PaddlePaddle/XGBoost), and storage systems (MySQL/LMDB). For instance, DownloadDeepLearningModel handles model files, while GenerateRsaKeyPairApi manages key lifecycle operations.

## Key Business Scenarios  
The module supports end-to-end federated learning scenarios: 1) Secure initialization (RSA key generation → CA certificate cache refresh → gateway connection testing); 2) Collaborative modeling (data sharding deduplication → PSI sample alignment → horizontal logistic regression training); 3) System operations (scheduled cleanup of inactive accounts → hot configuration updates → file shard uploads). Interaction modes blend synchronous CRUD (e.g., AccountService), asynchronous workflows (ModelExportService), and event-driven mechanisms (ApplicationListener), resembling a hybrid of workflow engines and message buses. Typical applications include cross-institution data fusion (Bloom filter deduplication), flowchart node management (BaseFlowGraph anti-circular dependency), and real-time communication (WebSocket duplex sessions). Functional completeness is reflected in multi-component coordination, such as project deletion triggering cascaded cleanup and model exports synchronously pushing keys to the Serving system.


### Package Internal Structure View

```mermaid
graph TD
    service --> base
    service --> config
    service --> api
    service --> database
    service --> constant
    service --> util
    service --> proto
    service --> exception
    service --> service
    service --> scheduled
    service --> onlinedemo
    service --> cache
    service --> dto
    service --> operation
    service --> listener
    service --> model
    service --> fusion
    service --> component

    base --> file_system
    base --> OnlineDemoApi.java
    base --> LoginAccountInfo.java
    file_system --> WeFeFileSystem.java

    config --> CertBeans.java
    config --> WebSocketConfig.java

    api --> crypto
    api --> global_config
    api --> account
    api --> online_demo
    api --> data_resource
    api --> storage
    api --> chat
    api --> dev
    api --> message
    api --> service
    api --> blacklist
    api --> partner_config
    api --> file
    api --> gateway
    api --> data_output_info
    api --> union
    api --> operation
    api --> project
    api --> datasource
    api --> member
    api --> model
    api --> component

    crypto --> GenerateRsaKeyPairApi.java

    global_config --> GlobalConfigUpdateApi.java
    global_config --> GetGlobalConfigApi.java

    account --> QueryMemberAccountsApi.java
    account --> QueryOnlineApi.java
    account --> ListAllApi.java
    account --> UpdateUiConfigApi.java
    account --> SsoLoginApi.java

    online_demo --> TianmiantechPageApi.java
    online_demo --> CheckAccountExistApi.java
    online_demo --> TianmiantechCallApi.java
    online_demo --> CreateOnlineDemoAccountApi.java

    data_resource --> table_data_set
    data_resource --> upload_task
    data_resource --> bloom_filter
    data_resource --> image_data_set
    data_resource --> UsageInProjectListApi.java
    data_resource --> ListTagsApi.java
    data_resource --> DataResourceQueryApi.java

    table_data_set --> column
    table_data_set --> ListServerLocalFilesApi.java
    table_data_set --> UpdateApi.java
    table_data_set --> AddApi.java
    table_data_set --> TableDataSetDeleteApi.java
    table_data_set --> DetailApi.java
    table_data_set --> PreviewApi.java
    column --> ListApi.java

    upload_task --> DataResourceUploadTaskDetailApi.java
    upload_task --> DataResourceUploadTaskQueryApi.java

    bloom_filter --> BloomFilterPreviewApi.java
    bloom_filter --> BloomFilterDeleteApi.java
    bloom_filter --> BloomFilterDataResourceListApi.java
    bloom_filter --> BloomFilterDetailApi.java
    bloom_filter --> BloomFilterAddApi.java
    bloom_filter --> BloomFilterUpdateApi.java

    image_data_set --> sample
    image_data_set --> ImageDataSetUpdateApi.java
    image_data_set --> ImageDataSetAddApi.java
    image_data_set --> ImageDataSetDetailApi.java
    image_data_set --> ImageDataSetDownloadApi.java
    image_data_set --> ImageDataSetDeleteApi.java
    sample --> ImageDataSetSampleDeleteApi.java
    sample --> ImageDataSetSampleQueryApi.java
    sample --> ImageDataSetSampleDownloadApi.java
    sample --> ImageDataSetSampleUpdateApi.java
    sample --> ImageDataSetSampleStatisticsApi.java

    storage --> PreviewDataSetApi.java

    chat --> QueryChatLastAccountApi.java
    chat --> AddChatLastAccountApi.java
    chat --> SendMessageApi.java
    chat --> UpdateToReadApi.java
    chat --> QueryChatDetailApi.java
    chat --> UnreadMessageIncreaseOneApi.java
    chat --> ResendMessageApi.java
    chat --> DeleteChatLastAccountApi.java

    dev --> ShowConfigApi.java

    message --> QueryApi.java
    message --> ReadApi.java
    message --> DetailApi.java

    service --> VersionApi.java
    service --> ServiceAvailableApi.java
    service --> AliveApi.java

    blacklist --> BlacklistApi.java
    blacklist --> BlacklistMemberApi.java
    blacklist --> DeleteApi.java
    blacklist --> AddApi.java

    partner_config --> QueryApi.java
    partner_config --> DeleteApi.java
    partner_config --> AddApi.java

    file --> security
    file --> FileUploadApi.java
    file --> MergeApi.java
    security --> CsvSecurityChecker.java
    security --> FileSecurityChecker.java
    security --> ExcelSecurityChecker.java
    security --> ImageSecurityChecker.java

    gateway --> TestConnectApi.java
    gateway --> GetMemberJobProgressApi.java
    gateway --> GetDerivedDataSetDetailApi.java
    gateway --> RedirectApi.java

    data_output_info --> PushModelToServingByProviderApi.java
    data_output_info --> ModelExportToFileApi.java
    data_output_info --> PushRsaKeyToServingApi.java
    data_output_info --> ModelExportController.java
    data_output_info --> PushModelToServingApi.java

    union --> data_resource
    union --> member_auth
    union --> MemberListApi.java
    union --> GetMemberMapApi.java
    union --> AbstractThroughUnionApi.java
    data_resource --> tag
    data_resource --> DataResourceQueryApi.java
    data_resource --> DataResourceDetailApi.java
    tag --> QueryTagApi.java
    tag --> QueryDefaultTagApi.java
    member_auth --> MemberAuthTypeQueryApi.java
    member_auth --> DownloadFileApi.java
    member_auth --> QueryRealnameAuthAgreementTemplateApi.java
    member_auth --> MemberFileUploadApi.java
    member_auth --> MemberRealnameAuthInfoQueryApi.java
    member_auth --> MemberRealnameAuthApi.java

    operation --> LogQueryApi.java

    project --> modeling
    project --> job
    project --> dataset
    project --> project
    project --> flow
    project --> member
    project --> fusion
    project --> node
    modeling --> QueryApi.java
    modeling --> DetailApi.java
    job --> task
    job --> PreviewJobApi.java
    job --> QueryApi.java
    job --> ResumeJobApi.java
    job --> DownloadLogApi.java
    job --> GetJobProgressApi.java
    job --> DetailApi.java
    job --> UpdateJobStatusApi.java
    job --> StopJobApi.java
    job --> ViewDataSetApi.java
    job --> OnJobFinishedApi.java
    task --> TaskProgressDetailApi.java
    task --> GetFeatureApi.java
    task --> DetailApi.java
    task --> GetResultHistoryApi.java
    task --> GetResultApi.java
    dataset --> ListApi.java
    dataset --> RawDataSetListApi.java
    dataset --> AddDataSetApi.java
    dataset --> QueryDerivedDataSetApi.java
    dataset --> GetFeaturesApi.java
    dataset --> RemoveDataSetApi.java
    dataset --> AuditDataSetApi.java
    project --> QueryApi.java
    project --> UpdateProjectApi.java
    project --> AddApi.java
    project --> TopProjectApi.java
    project --> DataInfoApi.java
    project --> DetailApi.java
    project --> AuditApi.java
    project --> CloseProjectApi.java
    project --> CountStatisticsApi.java
    flow --> ListFlowNodeApi.java
    flow --> AddFlowApi.java
    flow --> UpdateFlowBaseInfoApi.java
    flow --> QueryFlowTemplateApi.java
    flow --> StartFlowApi.java
    flow --> QueryDataIoTaskConfigApi.java
    flow --> GetProgressApi.java
    flow --> DeleteApi.java
    flow --> SaveFlowTemplateApi.java
    flow --> QueryDataIoTaskFeaturesApi.java
    flow --> UpdateFlowGraphApi.java
    flow --> DetailFlowApi.java
    flow --> FlowQueryApi.java
    flow --> AddOotFlowApi.java
    flow --> CopyFlowApi.java
    flow --> TopFlowApi.java
    flow --> FlowDataSetInfoApi.java
    flow --> ListFlowTableDataSetApi.java
    member --> audit
    member --> AddApi.java
    member --> ListInAllProjectApi.java
    member --> ListInProjectApi.java
    member --> ExitProjectApi.java
    member --> OnlineCheckApi.java
    member --> RemoveApi.java
    audit --> ProjectMemberAuditListApi.java
    audit --> AuditApi.java
    fusion --> result
    fusion --> actuator
    fusion --> task
    fusion --> member
    fusion --> HashOptionsEnumApi.java
    result --> ResultExportApi.java
    result --> ResultPreviewApi.java
    result --> TestDBConnectApi.java
    result --> ResultExportProgressApi.java
    actuator --> psi
    psi --> DownloadBFApi.java
    psi --> ReceiveResultApi.java
    psi --> ServerSynStatusApi.java
    psi --> ServerCloseApi.java
    psi --> PsiCryptoApi.java
    task --> ReceiveApi.java
    task --> InfoApi.java
    task --> PagingApi.java
    task --> UpdateApi.java
    task --> RestartApi.java
    task --> DeleteApi.java
    task --> AddApi.java
    task --> DeleteCallbackApi.java
    task --> AuditCallbackApi.java
    task --> DetailApi.java
    task --> AuditApi.java
    task --> TaskStatusApi.java
    member --> QueryProvidersApi.java
    node --> CheckExistVertModelComponentApi.java
    node --> UpdateApi.java
    node --> CheckExistEvaluationComponentApi.java
    node --> DetailApi.java

    datasource --> QueryApi.java
    datasource --> DeleteApi.java
    datasource --> AddApi.java
    datasource --> TestDBConnectApi.java

    member --> SyncMemberToServingApi.java
    member --> IsInitializedApi.java
    member --> ResetRsaKeyApi.java
    member --> SyncMemberToUnionApi.java
    member --> CheckMemberRouteConnectApi.java
    member --> GetMemberMachineLearningEnvApi.java
    member --> UpdateMemberInfoApi.java
    member --> UpdateMemberLogoApi.java
    member --> MemberAvailableCheckApi.java
    member --> InitializeApi.java
    member --> MemberDetailApi.java

    model --> deep_learning
    deep_learning --> DownloadInferResultApi.java
    deep_learning --> DownloadDataSetZipApi.java
    deep_learning --> StartInferApi.java
    deep_learning --> DownloadDataSetImageApi.java
    deep_learning --> DownloadModelApi.java
    deep_learning --> StopInferApi.java

    component --> ListApi.java

    database --> repository
    database --> entity
    database --> DataSourceConfig.java
    repository --> data_resource
    repository --> fusion
    repository --> TaskProgressRepository.java
    repository --> base
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

    constant --> Config.java
    constant --> BloomfilterAddMethod.java
    constant --> ServiceStatus.java
    constant --> ChatConstant.java
    constant --> DataSetAddMethod.java

    util --> primarykey
    util --> unique
    util --> ExcelBloomfilterReader.java
    util --> SqlTableDataSetReader.java
    util --> ExcelTableDataSetReader.java
    util --> AbstractBloomFilterReader.java
    util --> TlsUtil.java
    util --> CsvBloomFilterReader.java
    util --> CsvTableDataSetReader.java
    util --> SqlBloomFilterReader.java
    util --> AbstractTableDataSetReader.java
    primarykey --> FieldInfo.java
    primarykey --> PrimaryKeyUtils.java
    unique --> DataSetBloomUniqueFilter.java
    unique --> AbstractDataSetUniqueFilter.java
    unique --> ContainResult.java
    unique --> DataSetMemoryUniqueFilter.java

    proto --> meta
    proto --> TransferServiceProto.java
    proto --> TransferServiceGrpc.java
    meta --> storage
    meta --> basic
    storage --> StorageMetaProto.java
    basic --> GatewayMetaProto.java
    basic --> BasicMetaProto.java

    exception --> MemberGatewayException.java
    exception --> FlowNodeException.java

    service --> account
    service --> init
    service --> data_resource
    service --> checkpoint
    service --> globalconfig
    service --> ProjectMemberService.java
    service --> verificationcode
    service --> fusion
    service --> modelexport
    service --> FlowActionQueueService.java
    service --> TaskService.java
    service --> ProjectFlowNodeService.java
    service --> SystemInitializeService.java
    service --> FlowTemplateService.java
    service --> ProjectFlowService.java
    service --> ProjectDataSetService.java
    service --> ServingService.java
    service --> AbstractService.java
    service --> EmailService.java
    service --> PartnerConfigService.java
    service --> GatewayService.java
    service --> ChatUnreadMessageService.java
    service --> DataSetColumnService.java
    service --> MessageService.java
    service --> ChatLastAccountService.java
    service --> ModelOotRecordService.java
    service --> ProjectService.java
    service --> MemberChatService.java
    service --> BlacklistService.java
    service --> JobService.java
    service --> TaskResultService.java
    service --> DataSetStorageService.java
    service --> CertOperationService.java
    service --> FlowJobService.java
    service --> ServiceCheckService.java
    service --> CacheObjects.java
    service --> PrivacyDatabaseEncryptService.java
    service --> TaskProgressService.java
    service --> ProjectDataSetAuditService.java
    service --> FeatureDataOutputInfoService.java
    service --> DataSourceService.java
    service --> JobMemberService.java
    service --> BaseGatewayService.java
    service --> WebSocketServer.java
    service --> OperationLogService.java
    service --> ProjectFlowJobService.java
    service --> ProjectMemberAuditService.java
    account --> AccountService.java
    init --> MainfestType.java
    init --> AbstractManifest.java
    data_resource --> table_data_set
    data_resource --> bloom_filter
    data_resource --> add
    data_resource --> image_data_set
    data_resource --> DataResourceUploadTaskService.java
    data_resource --> AbstractDataResourceService.java
    data_resource --> DataResourceService.java
    table_data_set --> TableDataSetService.java
    bloom_filter --> BloomFilterTaskService.java
    bloom_filter --> BloomFilterStorageService.java
    bloom_filter --> BloomFilterService.java
    bloom_filter --> BloomFilterColumnService.java
    add --> BloomFilterAddServiceDataRowConsumer.java
    add --> TableDataSetAddServiceDataRowConsumer.java
    add --> ImageDataSetAddService.java
    add --> BloomFilterAddService.java
    add --> Table

# File List

| Name   | Type  | Description |
|-------|------|-------------|
| [dto](dto/_module.md) | package | The module uniformly manages the lifecycles of multi-type business entities, including data resources, messages, annotations, and task processing. It supports the entire federated learning workflow, encompassing task configuration, member topology management, data fusion, and paginated queries. Adopting a layered design, it relies on multiple frameworks to achieve standardized interfaces and state-driven interactions. |
| [component](component/_module.md) | package | Federated Learning Platform Component Collection, including modules for data interaction, feature engineering, machine learning modeling (Logistic Regression/XGBoost/Neural Networks), deep learning (PaddlePaddle image processing), and evaluation/validation. Designed with the strategy pattern, it supports horizontal/vertical/hybrid scenarios and features a unified interface specification (parameter validation-JSON configuration-result output). It relies on Java standard libraries and internal services. |
| [BoardService.java](BoardService.md) | file | BoardService serves as the entry point for SpringBoot applications, integrating scheduled and asynchronous tasks, custom component scanning, and permission control. It handles API exceptions and rate limiting while supporting RSA signature verification. |
| [service](service/_module.md) | package | The AccountService provides account management functionalities, relying on multiple services to support operations such as querying, filtering, and login. The GlobalConfigService manages global configurations, ensuring security and consistency. The ProjectService oversees the entire project lifecycle, including members, datasets, and statuses. The GatewayService handles message synchronization and gateway communication. The DataResourceService uniformly manages CRUD operations for various datasets. The Fusion module processes the lifecycle of data fusion tasks. ModelExport implements multi-language model code generation. The Checkpoint module monitors service health status. Other services include management functionalities for messages, chats, tasks, certificates, and more. |
| [fusion](fusion/_module.md) | package | Enumeration defines export states: Failed, Successful, In Progress. The module implements PSI task processing, including data dumping, state synchronization, and thread safety, relying on multiple services. It manages executor states and export progress, adopts a cache-first strategy, and supports task deduplication and progress queries. |
| [model](model/_module.md) | package | The JobBuilder class includes a dataSetVersion field to mark the image dataset version, optimizing download performance. BaseFlowGraph is an abstract base class for managing federated learning flow graphs, containing core attributes and methods such as tasks and nodes. FlowGraph inherits from BaseFlowGraph, supporting multiple initialization and node lookup functionalities. FlowGraphNode represents a flow graph node, containing attributes like depth and parent-child nodes, as well as task generation methods. |
| [listener](listener/_module.md) | package | AppListener monitors environment preparation events and logs them. ApplicationStartedListener handles application startup, initializes configurations, encrypts databases, loads certificates, etc. ApplicationReadyListener manages gateway whitelists and cleanup tasks after the startup is completed. |
| [operation](operation/_module.md) | package | BoardApiLogger inherits from AbstractApiLogger, ignores logging for specific APIs, saves operation logs to the database, and updates the account's last operation time. |
| [cache](cache/_module.md) | package | The `CaCertificateCache` class is a singleton-pattern CA certificate cache that uses `ConcurrentHashMap` to store certificate data, providing functionalities such as refreshing the cache, and retrieving single or all certificates. The inner class `CaCertificate` contains the attributes `id`, `name`, and `content`. |
| [onlinedemo](onlinedemo/_module.md) | package | Tianmian Tech service class inherits from an abstract class, containing URL and RSA key configurations, providing `through` and `request` methods to handle signed requests. The `hackOnDelete` method in `OnlineDemoBranchStrategy` verifies user permissions during online demos, allowing only creators to delete data. |
| [scheduled](scheduled/_module.md) | package | The AccountScheduledService manages accounts on a scheduled basis, executing hourly to disable inactive accounts after 90 days and delete them after 180 days. The OnlineDemoScheduledService cleans up demo environment data, including projects and logs, every 10 minutes. The CaCertificateScheduledService refreshes the CA certificate cache every 30 seconds. |
| [exception](exception/_module.md) | package | The `MemberGatewayException` is an exception class for handling member gateway errors, containing a member ID field. Its constructor initializes the ID and error message, with a default status code of `REMOTE_SERVICE_ERROR`. It overrides `getMessage` to return formatted information. The `FlowNodeException` represents a flowchart node exception, containing a `FlowGraphNode` field. Its constructor initializes the node and exception message, overrides `getMessage` to return a formatted message, and provides a `getNode` method. |
| [proto](proto/_module.md) | package | Distributed Communication and Storage Metadata Protocol, including endpoint management, state machine, and storage locator. Based on Protobuf, supports asynchronous event-driven architecture for cross-node routing and heterogeneous storage access. Includes gRPC service interfaces. |
| [util](util/_module.md) | package | Module 1 manages field metadata and generates primary keys, including the FieldInfo and PrimaryKeyUtils classes, with support for hash processing. Module 2 provides dataset deduplication functionality, featuring two strategies: Bloom filter and in-memory HashSet. Multiple Reader classes (Excel, CSV, SQL) inherit from an abstract class to read data, supporting header processing, row counting, and resource release. The TlsUtil class converts certificate formats. |
| [constant](constant/_module.md) | package | The Config class inherits from CommonConfig, loads dynamic path configuration files, and supports multiple environments. The BloomfilterAddMethod enum defines three data addition methods: HTTP upload, local file, and database. The ServiceStatus enum includes normal and offline states along with their descriptions. The ChatConstant class provides constants for chat message direction, status, and key-value pairs. The DataSetAddMethod enum defines three dataset addition methods. |
| [sdk](sdk/_module.md) | package | Manage member basic information and alliance data services, including the MemberBaseInfo data structure and the UnionService service class. Supports member status management, data resource sharing, permission checks, and asynchronous caching. Depends on Java libraries and caching frameworks. |
| [database](database/_module.md) | package | A generic data access layer based on Spring Data JPA, uniformly managing business entity persistence with support for CRUD, batch updates, and pagination. Key data structures include 40+ entity classes, relying on Spring Data JPA to ensure transactional safety. It supports full business lifecycle management, covering scenarios such as data preprocessing and task scheduling. |
| [api](api/_module.md) | package | GenerateRsaKeyPairApi generates RSA key pairs and returns the public key. The global configuration module provides configuration update and query functions. The account management module handles member information queries and UI configuration updates. The online demo module supports URL generation and account verification. The data resource module manages the lifecycle of multimodal data. The chat system module provides message sending/receiving and status updates. The message module supports CRUD operations for messages. The service status module checks version and availability. The blacklist module manages member additions, deletions, and queries. The partner configuration module handles CRUD operations. The file module implements upload merging and security checks. The gateway module provides connection checks and task queries. The model output module handles model deployment and file exports. The alliance module manages data resources and member authentication. The log module queries operation records. The federated learning module manages the entire project lifecycle. The data source module provides CRUD and connection testing. The member module manages alliance member information. The inference module supports the complete model inference workflow. The component module retrieves filtered component lists. |
| [config](config/_module.md) | package | CertBeans is a Java configuration class that provides the Bean definition for CertService. The WebSocketConfig configuration class registers WebSocket endpoints and resolves dependency injection issues. |
| [base](base/_module.md) | package | The WeFeFileSystem class manages file upload storage and directories, including the UseType enum to define file purposes, with subclasses handling model downloads and invocations. OnlineDemoApi is a runtime class annotation. The LoginAccountInfo singleton class manages logged-in user information, utilizing an expiring Map for storage. |


