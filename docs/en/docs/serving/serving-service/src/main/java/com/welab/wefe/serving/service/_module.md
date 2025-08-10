# Basic Information

|      |      |
|------|------|
| Name | service |
| Language | .java |
| Code Path | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service |
| Package Name | docs.serving.serving-service.src.main.java.com.welab.wefe.serving.service |
| Brief Description | Config Class: A Spring component that loads external configurations, defines file paths, email subjects, and other properties, with support for UTF-8 encoding.  XxxModelProcessor Class: Inherits from an abstract class, with empty implementations for pre-processing and post-processing methods.  Federated Learning Core API: Provides encrypted communication, member management, and other functionalities, designed in a RESTful style.  Prediction Engine: Supports federated prediction, including standard, batch, and debug modes.  ORM Layer: Implements data management using JPA, with 20+ entity classes.  Toolset: Includes signature verification, encryption, and more.  Enum Module: Defines service statuses and types.  Privacy Computing Framework: Handles PSI/PIR/SA requests.  Feature Management: Unifies the management of data sources and models.  Service Governance: Manages global configurations and model lifecycle.  Scheduled Tasks: Executes statistics and status maintenance.  DTO Management: Encapsulates business data interactions.  Log Processing: Records API logs to MySQL.  Startup Listener: Executes initialization tasks.  Feature Processing Framework: Annotation and SQL-driven.  ServingService Main Class: Spring Boot application startup configuration. |

# Description

## Overview  
This module is a core component collection of the federated learning service system, designed with a microservices architecture. Its primary responsibilities include system configuration management, federated prediction execution, data persistence, and secure communication. The interface specifications are hierarchically unified: configuration classes adopt Spring property injection (e.g., Config), processor classes follow the template method pattern (e.g., XxxModelProcessor), and the API layer inherits the AbstractApi base class to implement RESTful interactions. Key data structures are aggregated into four categories: system configurations (e.g., PSI batch size), prediction parameters (e.g., FederatedPredictParam), persistence models (e.g., PredictLogMySqlModel), and enumerated states (e.g., ServiceTypeEnum). External dependencies, after deduplication, include the Spring ecosystem (JPA/Cloud), encryption components (SM2/RSA), multi-database drivers (MySQL/Doris/Hive), and JNI calls. For example, Config manages SM2 keys, and PromoterPredictor coordinates multi-party predictions.  

## Core Business Scenarios  
The module supports the full lifecycle management of federated learning, with business processes consolidated into: 1) System initialization (key generation → configuration loading → service registration); 2) Federated prediction (feature acquisition → secure computation → result aggregation); 3) Service governance (log statistics → billing settlement → status tracking). The typical interaction pattern resembles a master-slave architecture, where PromoterPredictor coordinates multi-node computations, relying on a signature verification framework to ensure communication security. Functional completeness is reflected in the collaboration of the configuration center (Config), prediction engine (Predicter), persistence layer (Database), and service governance (Service). For instance, in a financial risk control scenario, a bank initializes via InitializeApi → invokes PromoterPredictor → records PredictLogMySqlModel → generates FeeDetailMysqlModel. API types cover encrypted communication, member management, model prediction, and scheduled tasks, with integration examples visible in the startup process of ServingService (loading processors → initializing listeners → launching API services).


### Package Internal Structure View

```mermaid
graph TD
    service --> config
    service --> processor
    service --> api
    service --> predicter
    service --> database
    service --> utils
    service --> enums
    service --> service_processor
    service --> manager
    service --> service
    service --> scheduler
    service --> dto
    service --> operation
    service --> listener
    service --> feature
    service --> ServingService.java

    config --> Config.java
    processor --> XxxModelProcessor.java
    api --> crypto
    api --> client
    api --> system
    api --> account
    api --> orderstatistics
    api --> partner
    api --> apirequestrecord
    api --> sa
    api --> predict
    api --> feeconfig
    api --> serviceorder
    api --> clientservice
    api --> paymentsrecords
    api --> logger
    api --> requeststatistics
    api --> file
    api --> feedetail
    api --> pir
    api --> operation
    api --> datasource
    api --> member
    api --> model

    crypto --> GenerateRsaKeyPairApi.java
    client --> QueryClientListApi.java
    client --> UpdateApi.java
    client --> SaveClientApi.java
    client --> QueryClientApi.java
    system --> InitializeUnionModeApi.java
    system --> ResetRsaKeyApi.java
    system --> GlobalConfigUpdateApi.java
    system --> UpdateRsaKeyByBoardApi.java
    system --> InitializeApi.java
    system --> GlobalConfigDetailApi.java
    system --> IsInitializeApi.java
    account --> SsoLoginApi.java
    account --> QueryAllApi.java
    orderstatistics --> QueryListApi.java
    orderstatistics --> DownloadApi.java
    orderstatistics --> SaveApi.java
    partner --> QueryPartnerListApi.java
    partner --> SavePartnerApi.java
    partner --> UpdateApi.java
    partner --> DetailPartnerApi.java
    partner --> QueryPartnerAllApi.java
    partner --> InitPartnerApi.java
    apirequestrecord --> QueryListApi.java
    apirequestrecord --> DownloadApi.java
    sa --> SecureAggregationForResultApi.java
    predict --> deep_learning
    predict --> PredictApi.java
    predict --> DebugApi.java
    predict --> SqlConfigTestApi.java
    predict --> PromoterApi.java
    predict --> ProviderApi.java
    deep_learning --> DeepLearningPredictApi.java
    feeconfig --> SaveApi.java
    feeconfig --> QueryApi.java
    serviceorder --> QueryListApi.java
    serviceorder --> DownloadApi.java
    serviceorder --> SaveApi.java
    clientservice --> ServiceUrlTestApi.java
    clientservice --> QueryListApi.java
    clientservice --> QueryApi.java
    clientservice --> UpdateApi.java
    clientservice --> ActivateServiceApi.java
    clientservice --> DeleteActivateServiceApi.java
    clientservice --> UpdateClientServiceInfoApi.java
    clientservice --> DetailApi.java
    clientservice --> UpdateStatusApi.java
    clientservice --> SaveApi.java
    clientservice --> UpdateActivateServiceApi.java
    paymentsrecords --> QueryListApi.java
    paymentsrecords --> DownloadApi.java
    paymentsrecords --> SaveApi.java
    logger --> StatisticsApi.java
    logger --> QueryApi.java
    logger --> DateTypeEnumApi.java
    logger --> ModelListApi.java
    requeststatistics --> QueryListApi.java
    file --> security
    file --> FileUploadApi.java
    file --> MergeApi.java
    security --> FileSecurityChecker.java
    feedetail --> QueryListApi.java
    pir --> PrivateInformationRetrievalForNaorPinkasResultsApi.java
    pir --> PrivateInformationRetrievalForRandomLegalApi.java
    pir --> PrivateInformationRetrievalForResultsApi.java
    pir --> PrivateInformationRetrievalForRandomApi.java
    operation --> LogQueryApi.java
    datasource --> QueryApi.java
    datasource --> QueryTablesApi.java
    datasource --> UpdateApi.java
    datasource --> DeleteApi.java
    datasource --> AddApi.java
    datasource --> TestDBConnectApi.java
    datasource --> QueryTableFieldsApi.java
    member --> QueryApi.java
    member --> DeleteApi.java
    member --> SaveApi.java
    model --> QueryApi.java
    model --> ProviderModelStatusCheckApi.java
    model --> ImportApi.java
    model --> PsiApi.java
    model --> UpdateModelApi.java
    model --> SaveModelApi.java
    model --> DetailApi.java
    model --> ModelStatusCheckApi.java
    model --> EnableApi.java

    predicter --> single
    predicter --> batch
    predicter --> Predictor.java
    single --> DebugProviderPredictor.java
    single --> PromoterPredictHelper.java
    single --> ProviderPredictor.java
    single --> DebugPromoterPredictor.java
    single --> PromoterPredictor.java
    batch --> BatchPromoterPredictor.java
    batch --> BatchProviderPredictor.java

    database --> repository
    database --> entity
    database --> config
    repository --> AccountRepository.java
    repository --> BaseServiceRepository.java
    repository --> FeeRecordRepository.java
    repository --> ClientServiceQueryRepository.java
    repository --> FeeDetailRepository.java
    repository --> ServiceOrderRepository.java
    repository --> base
    repository --> MemberRepository.java
    repository --> MessageRepository.java
    repository --> DataSourceRepository.java
    repository --> PredictStatisticsRepository.java
    repository --> ModelSqlConfigRepository.java
    repository --> TableModelRepository.java
    repository --> OperationLogRepository.java
    repository --> PaymentsRecordsRepository.java
    repository --> GlobalConfigRepository.java
    repository --> GlobalSettingRepository.java
    repository --> TableServiceRepository.java
    repository --> PredictLogRepository.java
    repository --> OrderStatisticsRepository.java
    repository --> ModelMemberRepository.java
    repository --> PartnerRepository.java
    repository --> ModelPredictScoreStatisticsRepository.java
    repository --> ClientRepository.java
    repository --> RequestStatisticsRepository.java
    repository --> PredictScoreStatisticsRepository.java
    repository --> ServiceCallLogRepository.java
    repository --> ApiRequestRecordRepository.java
    repository --> PsiServiceResultRepository.java
    repository --> FeeConfigRepository.java
    repository --> ClientServiceRepository.java
    repository --> VerificationCodeRepository.java
    repository --> ModelMemberBaseRepository.java
    repository --> ModelPredictScoreRecordRepository.java
    base --> BaseRepositoryFactoryBean.java
    base --> BaseRepositoryImpl.java
    base --> BaseRepository.java
    entity --> FeeDetailOutputModel.java
    entity --> PredictLogMySqlModel.java
    entity --> MessageMysqlModel.java
    entity --> PredictStatisticsMySqlModel.java
    entity --> GlobalSettingMySqlModel.java
    entity --> RequestStatisticsMysqlModel.java
    entity --> TableServiceMySqlModel.java
    entity --> GlobalConfigMysqlModel.java
    entity --> ClientServiceMysqlModel.java
    entity --> PsiServiceResultMysqlModel.java
    entity --> ModelSqlConfigMySqlModel.java
    entity --> AccountMySqlModel.java
    entity --> FeeConfigMysqlModel.java
    entity --> ModelPredictScoreStatisticsMySqlModel.java
    entity --> StatisticsSumModel.java
    entity --> BaseServiceMySqlModel.java
    entity --> ServiceOrderMysqlModel.java
    entity --> ModelPredictScoreRecordMySqlModel.java
    entity --> PartnerMysqlModel.java
    entity --> OperationLogMysqlModel.java
    entity --> VerificationCodeMysqlModel.java
    entity --> ServiceCallLogMysqlModel.java
    entity --> MemberMySqlModel.java
    entity --> PaymentsRecordsMysqlModel.java
    entity --> ClientServiceOutputModel.java
    entity --> AbstractBaseMySqlModel.java
    entity --> ApiRequestRecordMysqlModel.java
    entity --> ClientMysqlModel.java
    entity --> ModelMemberBaseModel.java
    entity --> FeeDetailMysqlModel.java
    entity --> DataSourceMySqlModel.java
    entity --> TableModelMySqlModel.java
    entity --> AbstractMySqlModel.java
    entity --> ModelMemberMySqlModel.java
    entity --> OrderStatisticsMysqlModel.java
    config --> DataSourceConfig.java

    utils --> deep_learning
    utils --> sign
    utils --> component
    utils --> SHA256Utils.java
    utils --> MD5Util.java
    utils --> ServiceUtil.java
    utils --> SerializeUtil.java
    utils --> ZipUtils.java
    utils --> RedisIntermediateCache.java
    utils --> ServingFileUtil.java
    utils --> SignUtils.java
    utils --> DeepLearningUtil.java
    sign --> AbstractVerifySignFunction.java
    sign --> BoardVerifySignFunction.java
    sign --> VerifySignUtil.java
    sign --> PartnerVerifySignFunction.java
    component --> ScoreCardComponentUtil.java

    enums --> DataResourceSource.java
    enums --> ServiceTypeEnum.java
    enums --> MemberModelStatusEnum.java
    enums --> DateTypeEnum.java
    enums --> ServiceOrderEnum.java
    enums --> CallByMeEnum.java
    enums --> ModelTypeEnum.java
    enums --> ServiceResultEnum.java
    enums --> PaymentsRecordStatusEnum.java
    enums --> PayTypeEnum.java
    enums --> QueryDateTypeEnum.java
    enums --> ServingModeEnum.java
    enums --> ServiceClientTypeEnum.java
    enums --> ServiceStatusEnum.java
    enums --> ClientStatusEnum.java
    enums --> ServiceCallStatusEnum.java
    enums --> PaymentsTypeEnum.java

    service_processor --> SAQueryServiceProcessor.java
    service_processor --> MultiPsiServiceProcessor.java
    service_processor --> ServiceProcessorUtils.java
    service_processor --> PirServiceProcessor.java
    service_processor --> PsiServiceProcessor.java
    service_processor --> ModelServiceProcessor.java
    service_processor --> MultiPirServiceProcessor.java
    service_processor --> AbstractServiceProcessor.java
    service_processor --> SAServiceProcessor.java

    manager --> FeatureManager.java
    manager --> JdbcManager.java
    manager --> ModelManager.java

    service --> globalconfig
    service --> ClientService.java
    service --> model
    service --> EmailService.java
    service --> TableModelService.java
    service --> ModelPredictScoreRecordService.java
    service --> ModelPredictScoreStatisticsService.java
    service --> PartnerService.java
    service --> ApiRequestRecordService.java
    service --> AccountService.java
    service --> ServiceCallLogService.java
    service --> FeeConfigService.java
    service --> PredictStatisticsService.java
    service --> MessageService.java
    service --> PredictLogService.java
    service --> TestTempService.java
    service --> RequestStatisticsService.java
    service --> PaymentsRecordsService.java
    service --> UnionServiceService.java
    service --> ModelMemberService.java
    service --> ClientServiceService.java
    service --> CacheObjects.java
    service --> PrivacyDatabaseEncryptService.java
    service --> ServiceOrderService.java
    service --> ModelService.java
    service --> DataSourceService.java
    service --> MemberService.java
    service --> ServiceService.java
    service --> OperationLogService.java
    service --> OrderStatisticsService.java
    service --> FeeDetailService.java
    service --> PsiServiceResultService.java
    service --> ModelSqlConfigService.java
    globalconfig --> GlobalConfigService.java
    globalconfig --> BaseGlobalConfigService.java
    model --> ModelImportService.java

    scheduler --> LogStatisticsScheduler.java
    scheduler --> AccountScheduledService.java
    scheduler --> OrderStatisticsScheduler.java
    scheduler --> PredictScoreStatisticsScheduler.java
    scheduler --> OrderToFeeDetailScheduler.java

    dto --> globalconfig
    dto --> ServiceOrderInput.java
    dto --> ModelSqlConfigOutput.java
    dto --> TreeNode.java
    dto --> ModelStatusOutput.java
    dto --> ServiceDetailOutput.java
    dto --> TreeNodeData.java
    dto --> OperationLogOutputModel.java
    dto --> OrderStatisticsInput.java
    dto --> FeeDetailInput.java
    dto --> BatchPredictInput.java
    dto --> AccountListAllOutputModel.java
    dto --> PagingOutput.java
    dto --> ServiceCallLogInput.java
    dto --> ServiceResultOutput.java
    dto --> MemberParams.java
    dto --> PagingInput.java
    globalconfig --> base
    globalconfig --> CaptchaSendChannelConfigModel.java
    globalconfig --> MailServerModel.java
    globalconfig --> UnionInfoModel.java
    globalconfig --> ServiceCacheConfigModel.java
    globalconfig --> GlobalConfigFlag.java
    globalconfig --> AliyunSmsConfigModel.java
    globalconfig --> GlobalConfigModel.java
    globalconfig --> IdentityInfoModel.java
    base --> AbstractConfigModel.java
    base --> GlobalConfigInput.java
    base --> ConfigModel.java
    base --> ConfigGroupConstant.java

    operation --> ServingApiLogger.java

    listener --> AutoPrivacyDatabaseEncryptListener.java
    listener --> ApplicationStartedListener.java

    feature --> code
    feature --> sql
    feature --> SqlFeatureDataHandler.java
    feature --> AbstractFeatureDataHandler.java
    feature --> CodeFeatureDataHandler.java
    code --> EmptyFeatureDataProcessor.java
    code --> FeatureProcessor.java
    code --> XxxFeatureDataProcessor.java
    code --> AbstractBatchFeatureDataProcessor.java
    code --> BatchFeatureProcessor.java
    code --> AbstractFeatureDataProcessor.java
    sql --> pg
    sql --> cassandra
    sql --> impala
    sql --> hive
    sql --> mysql
    sql --> SqlRuleUtil.java
    sql --> AbstractTemplate.java
    sql --> AbstractDruidTemplate.java
    pg --> PgSqlTemplate.java
    cassandra --> CassandraTemplate.java
    impala --> ImpalaTemplate.java
    hive --> HiveTemplate.java
    mysql --> MySqlTemplate.java
```

This flowchart presents the complete directory structure of the WeFe/serving project, starting from the top-level service node and expanding all submodules and files hierarchically. It primarily includes core components such as API interfaces, database operations, utility classes, enum definitions, service processors, management modules, and scheduled tasks. Each module is organized according to actual path relationships, clearly demonstrating the project's code organization and dependency structure, which facilitates developers' quick understanding of the system design.

# File List

| Name   | Type  | Description |
|-------|------|-------------|
| [config](config/_module.md) | package | Java configuration class containing attributes such as file paths, email subject content, PSI batch size, and key types, supporting external configuration injection and default value settings. |
| [predicter](predicter/_module.md) | package | This module provides federated learning prediction functionality, supporting standard/debug modes, including single-user/batch prediction, collaborator API calls, and feature retrieval. Key classes include Predictor, PromoterPredictHelper, etc., and rely on model and feature management services. It is suitable for multi-party data collaboration scenarios such as financial risk control. |
| [listener](listener/_module.md) | package | The AutoPrivacyDatabaseEncryptListener is a Spring component that listens for startup events, automatically checks and performs database encryption, and logs the process. The ApplicationStartedListener monitors startup, initializes caches, collects order statistics, saves fee details, handles exceptions, and logs events. |
| [api](api/_module.md) | package | The GenerateRsaKeyPairApi generates an RSA key pair and returns the public key. The client management module supports CRUD operations and validates IPs and public keys. The system module manages global configurations and keys. The account module handles SSO login and queries. The order statistics module provides query, download, and save functionalities. The partner module manages additions, deletions, modifications, and queries. The API log module supports querying and downloading. The security aggregation module processes aggregation results. The prediction module offers model prediction services. The billing module manages configurations. The service order module handles order management. The client service module manages the service lifecycle. The payment record module supports querying and downloading. The log module provides statistics and queries. The file module supports chunked uploads and merging. The expense details module queries expenses. The PIR module provides private information retrieval. The data source module manages database connections. The member module manages federation members. The model module manages the model lifecycle. The SaveMemberApi saves member information. |
| [service](service/_module.md) | package | The system manages global configuration initialization and maintenance, supporting multi-mode initialization and secure updates. It includes methods such as initialization checks, standalone/joint mode initialization, and configuration updates. Key data structures involve the AbstractConfigModel base class and encrypted fields. It relies on RSA key management and database storage layer. |
| [operation](operation/_module.md) | package | The ServingApiLogger inherits from AbstractApiLogger, skips logging for specific APIs, saves operation logs to the database, and updates the account's last operation time. |
| [ServingService.java](ServingService.md) | file | This is a Spring Boot application startup class that excludes data source auto-configuration, enables scheduled tasks, and customizes component scanning naming rules. The main method is launched via Launcher, configured with API permission validation logic, and initializes the model and feature processors. It also implements application context injection functionality. |
| [feature](feature/_module.md) | package | The feature processing framework provides single/batch modes, including abstract classes and annotation registration mechanisms, supporting null handling and extensions. The database module encapsulates multi-database JDBC operations, including connection pool management and SQL validation. SqlFeatureDataHandler implements multi-database queries, while CodeFeatureDataHandler manages processor mappings through reflection. |
| [dto](dto/_module.md) | package | Annotation-driven global configuration management module, automatically collects and categorizes configuration models, supports grouped retrieval. Includes multiple DTO classes such as ServiceOrderInput, TreeNode, etc., for handling service orders, tree structures, model states, and other data. Provides pagination, logging, and member parameter management functionalities. |
| [scheduler](scheduler/_module.md) | package | The LogStatisticsScheduler logs statistical information with an initial delay of 5 seconds and a fixed delay of 120 seconds. The AccountScheduledService processes inactive accounts every 10 minutes, with an initial delay of 10 seconds. The OrderStatisticsScheduler collects order data statistics every minute. The PredictScoreStatisticsScheduler refreshes predicted score statistics every 5 minutes. The OrderToFeeDetailScheduler processes fee records hourly. |
| [manager](manager/_module.md) | package | The FeatureManager manages feature data and caches data sources with thread safety. JdbcManager is deprecated, supporting multiple database connections and operations. The ModelManager handles model states, providing caching and synchronization methods. |
| [service_processor](service_processor/_module.md) | package | The SAQueryServiceProcessor handles secure aggregation queries using DH key exchange; the MultiPsiServiceProcessor manages multi-client PSI queries; the ServiceProcessorUtils maintains service type mappings; the PirServiceProcessor processes private information retrieval; the PsiServiceProcessor implements core PSI service functionality; the ModelServiceProcessor handles model predictions; the MultiPirServiceProcessor manages multiple PIR requests; the AbstractServiceProcessor serves as the abstract base class; the SAServiceProcessor executes SQL queries and caches results. |
| [enums](enums/_module.md) | package | The DataResourceSource enum defines data source types: local file, uploaded file, database. The ServiceTypeEnum enum defines eight service types, including query statistics and model services. The MemberModelStatusEnum enum defines member model states: offline, unavailable, available. The DateTypeEnum enum defines four date granularities: month, day, hour, minute. The ServiceOrderEnum enum defines three order statuses: success, failure, in progress. The CallByMeEnum enum defines whether to call: yes, no. The ModelTypeEnum enum defines model types: machine learning, deep learning. The ServiceResultEnum enum defines six service result status codes. The PaymentsRecordStatusEnum enum defines payment statuses: normal, reversal. The PayTypeEnum enum defines two payment types: postpaid, prepaid. The QueryDateTypeEnum enum defines four date query types. The ServingModeEnum enum defines service modes: independent, joint. The ServiceClientTypeEnum enum defines client types: activated, opened. The ServiceStatusEnum enum defines service statuses: enabled, disabled. The ClientStatusEnum enum defines client statuses: normal, deleted. The ServiceCallStatusEnum enum defines five call statuses. The PaymentsTypeEnum enum defines payment types: recharge, expenditure. |
| [utils](utils/_module.md) | package | Extensible signature verification framework supporting multiple strategy patterns, including RSA signature verification, identity verification, and other functionalities. Includes utility classes for encryption (SHA256, MD5), serialization, Redis cache operations, file processing, and deep learning service invocation. |
| [database](database/_module.md) | package | An enhanced repository layer based on Spring Data JPA, providing unified data access, audit logging, dynamic field updates, and SQL query conversion. Supports complex queries, multi-table joins, and cross-database aggregation, suitable for financial-grade data services. The data persistence layer for federated learning services implements ORM operations through JPA entity mapping, covering full lifecycle data management. Configuration classes support multi-data source environments, defining primary data sources, entity scan paths, and transaction management. |
| [processor](processor/_module.md) | package | This is a model processor class named XxxModelProcessor, which inherits from AbstractModelProcessor. It includes preprocessing (preprocess) and postprocessing (postprocess) methods for handling logic before and after model prediction. |


