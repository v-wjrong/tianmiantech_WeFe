# Basic Information

|      |      |
|------|------|
| Name | service |
| Language | .java |
| Code Path | WeFe/fusion/fusion-service/src/main/java/com/welab/wefe/data/fusion/service |
| Package Name | docs.fusion.fusion-service.src.main.java.com.welab.wefe.data.fusion.service |
| Brief Description | The core system of the federated learning platform includes control, data, and task modules, supporting the entire workflow from initialization to data management and task scheduling. It features a layered architecture design, unified interface standards, and integrates key data structures with multiple service components. |

# Description

## Overview  
This module serves as the core management system of the federated learning platform, adopting a layered architecture design that integrates system control, data management, task scheduling, and privacy computing functionalities. Its core responsibilities include: 1) achieving data persistence through a hierarchical storage system (MySQL/MergeTree); 2) ensuring secure cross-institutional data alignment based on the PSI (Private Set Intersection) algorithm; 3) providing a full lifecycle management toolkit (Bloom filters/primary key generation, etc.). The interface specifications uniformly employ JPA annotations and RESTful style, such as deriving various APIs from the AbstractApi base class and implementing extended queries via @Query. Key data structures encompass paginated result sets, encrypted business entities (e.g., GlobalConfigMysqlModel), and PSI execution parameters (e/N/d). External dependencies include Spring Data JPA, RSA encryption components, connection pool management (e.g., HikariCP), and multiple database drivers (MySQL/Hive/Impala).  

## Key Business Scenarios  
The module supports end-to-end federated learning process management, with a typical workflow as follows: 1) system initialization (generating RSA keys/validating memberName); 2) data preparation (DatasetApi managing CSV/Excel parsing); 3) secure computation (PsiClientActuator executing encrypted sharding); 4) result callback (TaskResultManager dynamically creating tables for storage). The interaction model combines the producer-consumer pattern (batch processing 10,000 rows of data) with state machine-driven operations (TaskStatus managing 7 states). Functional completeness is reflected in: encrypted validation (≤5 field combinations), thread-safe operations (ConcurrentHashMap managing tasks), and exception handling chains (StatusCodeWithException). Integration use cases span from basic configurations (DataSourceConfig multi-data sources) to complex business scenarios (RSA-PSI algorithm switching), resembling a distributed ETL console.


### Package Internal Structure View

```mermaid
graph TD
    service --> api
    service --> repo
    service --> database
    service --> utils
    service --> enums
    service --> actuator
    service --> manager
    service --> service
    service --> scheduled
    service --> dto
    service --> operation
    service --> task
    service --> listener
    service --> config
    service --> FusionService.java
    
    api --> system
    api --> account
    api --> partner
    api --> bloomfilter
    api --> thirdparty
    api --> file
    api --> dataset
    api --> operation
    api --> task
    api --> datasource
    
    system --> IsInitializedApi.java
    system --> ResetRsaKeyApi.java
    system --> OptionsApi.java
    system --> GlobalConfigUpdateApi.java
    system --> GetGlobalConfigApi.java
    system --> TaskOverviewApi.java
    system --> InitializeApi.java
    system --> ConfigApi.java
    
    account --> SsoLoginApi.java
    
    partner --> PagingApi.java
    partner --> UpdateApi.java
    partner --> DeleteApi.java
    partner --> AddApi.java
    partner --> CheckApi.java
    
    bloomfilter --> QueryApi.java
    bloomfilter --> DetailAndPreviewApi.java
    bloomfilter --> DeleteApi.java
    bloomfilter --> AddApi.java
    bloomfilter --> DetailApi.java
    bloomfilter --> GetBloomFilterStateApi.java
    bloomfilter --> PreviewApi.java
    
    thirdparty --> CallbackApi.java
    thirdparty --> RemoteCheckApi.java
    
    file --> MergeApi.java
    file --> UploadApi.java
    
    dataset --> GetDataSetStateApi.java
    dataset --> QueryApi.java
    dataset --> DetailAndPreviewApi.java
    dataset --> UpdateApi.java
    dataset --> DeleteApi.java
    dataset --> AddApi.java
    dataset --> DetailApi.java
    dataset --> GetHeadersApi.java
    dataset --> PreviewApi.java
    
    operation --> LogQueryApi.java
    
    task --> ReceiveApi.java
    task --> InfoApi.java
    task --> PagingApi.java
    task --> UpdateApi.java
    task --> DeleteApi.java
    task --> AddApi.java
    task --> DetailApi.java
    task --> TaskStatusApi.java
    task --> StopTaskApi.java
    task --> HandleApi.java
    
    datasource --> OverviewApi.java
    datasource --> QueryApi.java
    datasource --> UpdateApi.java
    datasource --> DeleteApi.java
    datasource --> AddApi.java
    datasource --> TestDBConnectApi.java
    
    repo --> impl
    repo --> Storage.java
    repo --> AbstractStorage.java
    
    impl --> MysqlStorage.java
    
    database --> repository
    database --> entity
    database --> DataSourceConfig.java
    
    repository --> DataSetRepository.java
    repository --> base
    repository --> DataSourceRepository.java
    repository --> BloomFilterRepository.java
    repository --> OperationLogRepository.java
    repository --> GlobalConfigRepository.java
    repository --> GlobalSettingRepository.java
    repository --> PartnerRepository.java
    repository --> TaskRepository.java
    repository --> FieldInfoRepository.java
    repository --> AccountRepository.java
    repository --> TaskResultRepository.java
    repository --> VerificationCodeRepository.java
    
    base --> BaseRepositoryFactoryBean.java
    base --> BaseRepositoryImpl.java
    base --> BaseRepository.java
    
    entity --> AbstractBaseMySqlModel.java
    entity --> TaskMySqlModel.java
    entity --> DataSetMySqlModel.java
    entity --> TaskResultMySqlModel.java
    entity --> GlobalSettingMySqlModel.java
    entity --> DataSetColumnOutputModel.java
    entity --> GlobalConfigMysqlModel.java
    entity --> BloomFilterMySqlModel.java
    entity --> PartnerMySqlModel.java
    entity --> OperationLogMysqlModel.java
    entity --> VerificationCodeMysqlModel.java
    entity --> FieldInfoMySqlModel.java
    entity --> AccountMysqlModel.java
    entity --> DataSourceMySqlModel.java
    entity --> AbstractMySqlModel.java
    
    utils --> bf
    utils --> primarykey
    utils --> dataresouce
    utils --> unique
    utils --> ByteUtils.java
    utils --> AbstractDataSetReader.java
    utils --> CsvDataSetReader.java
    utils --> ExcelDataSetReader.java
    utils --> FileSecurityChecker.java
    utils --> SocketUtils.java
    utils --> FusionUtils.java
    
    bf --> BloomFilterUtils.java
    bf --> BloomFilters.java
    bf --> BitArray.java
    
    primarykey --> PrimaryKeyUtils.java
    primarykey --> FieldInfo.java
    
    dataresouce --> DataResouceHelper.java
    
    unique --> DataSetBloomUniqueFilter.java
    unique --> AbstractDataSetUniqueFilter.java
    unique --> ContainResult.java
    unique --> DataSetMemoryUniqueFilter.java
    
    enums --> RoleType.java
    enums --> DBType.java
    enums --> Options.java
    enums --> TaskStatus.java
    enums --> DataResourceType.java
    enums --> DataResourceSource.java
    enums --> AlgorithmType.java
    enums --> CallbackType.java
    enums --> Progress.java
    enums --> ActionType.java
    enums --> PSIActuatorRole.java
    enums --> PSIActuatorStatus.java
    
    actuator --> rsapsi
    actuator --> AbstractActuator.java
    
    rsapsi --> PsiClientActuator.java
    rsapsi --> AbstractPsiActuator.java
    rsapsi --> PsiServerActuator.java
    
    manager --> TaskResultManager.java
    manager --> ActuatorManager.java
    manager --> JdbcManager.java
    
    service --> bloomfilter
    service --> globalconfig
    service --> dataset
    service --> TaskService.java
    service --> SystemInitializeService.java
    service --> PartnerService.java
    service --> FusionStorageService.java
    service --> AccountService.java
    service --> AbstractService.java
    service --> DataStorageService.java
    service --> FieldInfoService.java
    service --> TaskResultService.java
    service --> CallbackService.java
    service --> CacheObjects.java
    service --> PrivacyDatabaseEncryptService.java
    service --> DataSourceService.java
    service --> GetHeadersService.java
    service --> ThirdPartyService.java
    service --> OperationLogService.java
    
    bloomfilter --> BloomFilterAddServiceDataRowConsumer.java
    bloomfilter --> BloomFilterService.java
    bloomfilter --> BloomFilterAddService.java
    bloomfilter --> GetBloomFilterStateService.java
    
    globalconfig --> GlobalConfigService.java
    globalconfig --> MailServerModel.java
    globalconfig --> BaseGlobalConfigService.java
    
    dataset --> DataSetAddService.java
    dataset --> GetDataSetStateService.java
    dataset --> DataSetAddServiceDataRowConsumer.java
    dataset --> DataSetService.java
    dataset --> DataSetStorageHelper.java
    
    scheduled --> AccountScheduledService.java
    
    dto --> vo
    dto --> entity
    dto --> base
    
    vo --> AccountInputModel.java
    vo --> AccountOutputModel.java
    
    entity --> bloomfilter
    entity --> globalconfig
    entity --> dataset
    entity --> DataSourceOverviewOutput.java
    entity --> TaskOverviewOutput.java
    entity --> OperationLogOutputModel.java
    entity --> PartnerOutputModel.java
    entity --> AbstractOutputModel.java
    entity --> TaskOutput.java
    
    bloomfilter --> BloomfilterOutputModel.java
    bloomfilter --> BloomfilterDetailOutputModel.java
    
    globalconfig --> GlobalConfigInput.java
    globalconfig --> MemberInfoModel.java
    globalconfig --> FusionConfigModel.java
    
    dataset --> DataSetOutputModel.java
    dataset --> DataSetPreviewOutputModel.java
    dataset --> DataSetDetailOutputModel.java
    dataset --> DataSetStateOutputModel.java
    
    base --> PagingOutput.java
    base --> PagingInput.java
    
    operation --> FusionApiLogger.java
    
    task --> PsiClientTask.java
    task --> AbstractTask.java
    task --> PsiServerTask.java
    task --> AbstractPsiTask.java
    
    listener --> AutoPrivacyDatabaseEncryptListener.java
    
    config --> Config.java
```

This flowchart illustrates the complete project structure of WeFe Data Fusion Service, comprising 13 main modules and hundreds of submodules. Core modules include the API interface layer, service layer, database layer, and utilities layer, forming a clear hierarchical relationship. The API module is subdivided into 10 submodules such as system and account, each containing multiple concrete API implementation classes. The service module implements business logic, including core services like bloomfilter. The database module manages data persistence, encompassing submodules such as repository and entity. The overall structure is well-organized with distinct layers, adhering to the single responsibility principle and modern microservices architecture design principles.

# File List

| Name   | Type  | Description |
|-------|------|-------------|
| [scheduled](scheduled/_module.md) | package | The AccountScheduledService scheduled task class runs every 10 minutes, automatically disabling accounts inactive for 90 days and deleting those inactive for 180 days, with logs recorded. |
| [operation](operation/_module.md) | package | FusionApiLogger inherits from AbstractApiLogger, ignores logs for specific APIs, saves logs to the database, and updates the account's last operation time. |
| [listener](listener/_module.md) | package | Automatic database encryption listener, which checks configurations and performs encryption services upon application startup, while logging operation records and exceptions. |
| [FusionService.java](FusionService.md) | file | A SpringBoot application integrates scheduling and asynchronous tasks, customizes component scanning paths, implements API permission verification and RSA signature validation, and launches and manages the application context through Launcher. |
| [config](config/_module.md) | package | The Config class inherits from CommonConfig, loads external configuration files via @PropertySource, and contains properties such as SMS verification code sending channels, Alibaba Cloud SMS configurations, and server IPs, providing getter/setter methods. |
| [task](task/_module.md) | package | PsiClientTask extends AbstractPsiTask and handles PSI client tasks. AbstractTask is an abstract class that manages task workflows. PsiServerTask extends AbstractPsiTask and handles PSI server tasks. AbstractPsiTask is the abstract base class for handling PSI executor tasks. |
| [dto](dto/_module.md) | package | The account module handles data validation and desensitization, the federated learning module manages data and tasks, and the pagination module encapsulates pagination query functionality. |
| [service](service/_module.md) | package | The Bloom Filter Management Module is responsible for creation, updates, queries, and monitoring, supporting multithreading and encrypted verification. The Global Configuration Module manages member information and email settings, supporting group operations. The Dataset Module handles creation, status tracking, and batch processing. The Task Service manages task status, statistics, and request processing. The System Initialization Service checks and initializes system configurations. The Partner Service manages partner data. The Storage Service provides database operation functionalities. The Single Sign-On Service handles account initialization and updates. The Abstract Service offers logging capabilities. The Data Storage Service manages table operations. The Field Information Service processes column names and attributes. The Task Result Service manages result tables. The Callback Service handles task callbacks. The Cache Utility Class manages static data. The Privacy Data Encryption Service handles database encryption. The Data Source Service manages data source connections and validation. The Header Service retrieves dataset headers. The Third-Party Service handles interactions with partners. The Operation Log Service queries log records. |
| [manager](manager/_module.md) | package | The TaskResultManager manages task result data, supporting table creation, insertion, and batch saving. The ActuatorManager manages task actuators, providing thread-safe task and Bloom filter operations. The JdbcManager is a deprecated JDBC utility class that supports multiple database connections and queries. |
| [actuator](actuator/_module.md) | package | The PsiClientActuator and PsiServerActuator form the PSI dual-end module, which employs RSA encryption and Bloom filters to achieve secure data alignment. The client performs encrypted comparison while the server processes requests, supporting cross-institution data matching such as financial risk control. AbstractActuator is an abstract class containing initialization, processing, and storage methods, utilizing LongAdder for counting. |
| [enums](enums/_module.md) | package | Multiple enumeration types are defined: RoleType (promoter/provider), DBType (6 database types), Options (4 processing methods), TaskStatus (7 task statuses), DataResourceType (2 resource types), DataResourceSource (3 sources), AlgorithmType (2 algorithms), CallbackType (4 callback statuses), Progress (6 progress stages), ActionType (5 operations), PSIActuatorRole (2 roles), PSIActuatorStatus (6 statuses). |
| [utils](utils/_module.md) | package | Bloom filter enables high-performance data deduplication. The primary key generation module supports multiple hash algorithms. The data parsing tool processes CSV/Excel/DB data sources. The deduplication module offers both Bloom filter and in-memory set strategies. The file type checker restricts formats to xls/xlsx/csv. The Socket tool manages connection retries. The byte utility class implements conversions between integers and byte arrays. |
| [database](database/_module.md) | package | A universal repository framework based on Spring Data JPA, providing standardized data access and native SQL extensions, supporting multi-entity CRUD, transactional operations, and complex queries. Includes the MySqlModel series of entities, dependent on Spring Data JPA and Hibernate. Used for data fusion services, covering the entire lifecycle including task management and dataset processing. The configuration class DataSourceConfig sets up data sources and JPA parameters. |
| [repo](repo/_module.md) | package | MysqlStorage inherits from AbstractStorage, implementing MySQL operations: table creation, table deletion, insertion, batch insertion, and counting, including exception handling and connection pool management. Storage defines abstract storage methods, while AbstractStorage extends functionality and implements resource management. |
| [api](api/_module.md) | package | The system management module is responsible for initialization, configuration, and key management; the partner module provides CRUD functionality; the Bloom filter module supports CRUD and status queries; the third-party service module handles callbacks and status checks; the file module manages chunked uploads and merging; the dataset module implements lifecycle management; the log module queries operation records; the task module manages the full task lifecycle; the data source module handles data source CRUD and connection testing. |


