# Basic Information

|      |      |
|------|------|
| Name | wefe |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe |
| Package Name | docs.board.board-service.src.main.java.com.welab.wefe |
| Brief Description | The module system encompasses the full-stack functionality of the federated learning platform, including file system management, session state maintenance, Spring Bean configuration, data persistence, API services, scheduled tasks, exception handling, and modularized machine learning workflows. The core modules provide file lifecycle management, RESTful interfaces, JPA data operations, and distributed communication protocols, supporting both horizontal and vertical federated learning scenarios. Adopting a layered design, it integrates technologies such as Spring, gRPC, and cryptographic libraries to enable end-to-end collaborative workflows from data preprocessing to model training. |

# Description

## Overview  
This module serves as the core service matrix of the federated learning platform, integrating capabilities such as file system management, session state maintenance, Spring container configuration, data persistence, and distributed communication, akin to an enterprise-level AI collaboration hub. Unified interface standards encompass RESTful APIs (layered inheritance of AbstractApi), JPA specifications (BaseRepository extensions), and Protobuf/gRPC protocols (TransferServiceGrpc). Key data structures form a multi-dimensional system: business entity classes (JobMySqlModel), validation models (Input annotated with @Check), enumerated constants (ServiceStatus), and transmission metadata (TransferMeta sharding units). External dependencies are concentrated in the Spring ecosystem (JPA/WebSocket), cryptographic components (RSA/AES), machine learning frameworks (PaddlePaddle/XGBoost), and storage systems (MySQL/LMDB). For instance, DownloadDeepLearningModel handles model files, while GenerateRsaKeyPairApi manages key lifecycle operations.

## Key Business Scenarios  
The module supports end-to-end federated learning scenarios: 1) Secure initialization (RSA key generation → CA certificate cache refresh → gateway connection testing); 2) Collaborative modeling (data sharding deduplication → PSI sample alignment → horizontal logistic regression training); 3) System operations (scheduled cleanup of inactive accounts → hot configuration updates → file sharding uploads). Interaction modes blend synchronous CRUD (e.g., AccountService), asynchronous workflows (ModelExportService), and event-driven mechanisms (ApplicationListener), resembling a hybrid of workflow engines and message buses. Typical applications include cross-institution data fusion (Bloom filter deduplication), flowchart node management (BaseFlowGraph anti-circular dependencies), and real-time communication (WebSocket duplex sessions). Functional completeness is reflected in multi-component coordination, such as project deletion triggering cascaded cleanup and model exports synchronously pushing keys to the Serving system.


### Package Internal Structure View

```mermaid
graph TD
    board --> service
    board --> database
    board --> constant
    board --> util
    board --> proto
    board --> exception
    board --> model
    board --> fusion
    board --> component
    board --> dto
    board --> operation
    board --> listener
    board --> scheduled
    board --> onlinedemo
    board --> cache
    
    service --> account
    service --> init
    service --> data_resource
    service --> checkpoint
    service --> globalconfig
    service --> verificationcode
    service --> fusion
    service --> modelexport
    service --> FlowActionQueueService
    service --> TaskService
    service --> ProjectFlowNodeService
    service --> SystemInitializeService
    service --> FlowTemplateService
    service --> ProjectFlowService
    service --> ProjectDataSetService
    service --> ServingService
    service --> AbstractService
    service --> EmailService
    service --> PartnerConfigService
    service --> GatewayService
    service --> ChatUnreadMessageService
    service --> DataSetColumnService
    service --> MessageService
    service --> ChatLastAccountService
    service --> ModelOotRecordService
    service --> ProjectService
    service --> MemberChatService
    service --> BlacklistService
    service --> JobService
    service --> TaskResultService
    service --> DataSetStorageService
    service --> CertOperationService
    service --> FlowJobService
    service --> ServiceCheckService
    service --> CacheObjects
    service --> PrivacyDatabaseEncryptService
    service --> TaskProgressService
    service --> ProjectDataSetAuditService
    service --> FeatureDataOutputInfoService
    service --> DataSourceService
    service --> JobMemberService
    service --> BaseGatewayService
    service --> WebSocketServer
    service --> OperationLogService
    service --> ProjectFlowJobService
    service --> ProjectMemberAuditService
    
    data_resource --> table_data_set
    data_resource --> bloom_filter
    data_resource --> add
    data_resource --> image_data_set
    data_resource --> DataResourceUploadTaskService
    data_resource --> AbstractDataResourceService
    data_resource --> DataResourceService
    
    database --> repository
    database --> entity
    database --> DataSourceConfig
    
    repository --> data_resource
    repository --> fusion
    repository --> base
    repository --> TaskProgressRepository
    repository --> DataSourceRepository
    repository --> ChatLastAccountRepository
    repository --> ChatUnreadMessageRepository
    repository --> DataSetColumnRepository
    repository --> ModelOotRecordRepository
    repository --> OperationLogRepository
    repository --> JobMemberRepository
    repository --> GlobalConfigRepository
    repository --> ProjectMemberAuditRepository
    repository --> DataOutputInfoRepository
    repository --> OutputModelRepository
    repository --> PartnerConfigRepository
    repository --> TaskRepository
    repository --> CertInfoRepository
    repository --> FeatureJobMemberRepository
    repository --> MemberChatRepository
    repository --> FlowActionLogRepository
    repository --> BlacklistRepository
    repository --> FlowTemplateRepository
    repository --> MessageRepository
    repository --> CertKeyInfoRepository
    repository --> AccountRepository
    repository --> TrackingMetricRepository
    repository --> ImageDataSetSampleRepository
    repository --> ProjectFlowNodeRepository
    repository --> ProjectMemberRepository
    repository --> ProjectDataSetRepository
    repository --> FlowActionQueueRepository
    repository --> MessageQueueRepository
    repository --> TaskContextRepository
    repository --> JobRepository
    repository --> CertRequestInfoRepository
    repository --> RoleCountsRepository
    repository --> TaskResultRepository
    repository --> VerificationCodeRepository
    repository --> ProjectFlowRepository
    repository --> ProjectRepository
    
    entity --> cert
    entity --> data_resource
    entity --> job
    entity --> chat
    entity --> data_set
    entity --> flow
    entity --> fusion
    entity --> base
    entity --> MessageMysqlModel
    entity --> PartnerConfigMysqlModel
    entity --> OutputModelMysqlModel
    entity --> GlobalConfigMysqlModel
    entity --> BlacklistMysqlModel
    entity --> OperationLogMysqlModel
    entity --> VerificationCodeMysqlModel
    entity --> DataSourceMysqlModel
    entity --> TrackingMetricMysqlModel
    entity --> AccountMysqlModel
    entity --> DataOutputInfoMysqlModel
    
    dto --> vo
    dto --> kernel
    dto --> entity
    dto --> serving
    dto --> union
    dto --> fusion
    dto --> base
    
    vo --> data_resource
    vo --> message
    vo --> data_set
    vo --> RoleCounts
    vo --> AuditStatusCounts
    vo --> FeatureOutput
    vo --> JobMemberWithDataSetOutputModel
    vo --> OnlineAccountOutput
    vo --> AccountInputModel
    vo --> JobArbiterInfo
    vo --> JobProgressOutput
    vo --> ProjectFlowStatisticsResult
    vo --> FlowDataSetOutputModel
    
    component --> base
    component --> modeling
    component --> deep_learning
    component --> enums
    component --> temp
    component --> feature
    component --> EvaluationComponent
    component --> DataIOComponent
    component --> SegmentComponent
    component --> OotComponent
    component --> TableDataSetFeatureTracer
    component --> Components
    component --> IntersectionComponent
    
    base --> filter
    base --> io
    base --> dto
    base --> AbstractComponent
    
    modeling --> HorzLRComponent
    modeling --> HorzNNComponent
    modeling --> AbstractModelingComponent
    modeling --> VertSecureBoostComponent
    modeling --> HorzSecureBoostComponent
    modeling --> ScoreCardComponent
    modeling --> VertLRComponent
    modeling --> MixLrComponent
    modeling --> VertNNComponent
    modeling --> MixSecureBoostComponent
    
    deep_learning --> PaddleClassifyComponent
    deep_learning --> PaddleDetectionComponent
    deep_learning --> ImageDataIOComponent
    deep_learning --> AbstractDeepLearningComponent
    
    feature --> HorzFeatureBinningComponent
    feature --> FeatureTransformComponent
    feature --> VertFilterComponent
    feature --> MixBinningComponent
    feature --> FeatureStandardizedComponent
    feature --> MixStatisticComponent
    feature --> BinningComponent
    feature --> HorzOneHotComponent
    feature --> FillMissingValueComponent
    feature --> FeatureStatisticsComponent
    feature --> HorzStatisticComponent
    feature --> VertOneHotComponent
    feature --> VertPCAComponent
    feature --> VertPearsonComponent
    feature --> FeatureCalculationComponent
    feature --> FeaturePsiComponent
    feature --> FeatureSelectionComponent
```

This flowchart illustrates the complete module structure of the WeFe/board/board-service project, comprising 15 top-level modules and over 100 secondary modules. Core modules include service (business services), database (database-related), component (component system), and dto (data transfer objects). The service module is further divided into 23 sub-services such as account and data_resource, while the database module consists of two major branches: repository and entity. The component system adopts a layered design, incorporating specialized components for modeling, deep learning, and feature engineering. The overall architecture demonstrates clear hierarchical relationships, with modules interacting through well-defined interfaces, reflecting the modular design philosophy of complex business systems.

# File List

| Name   | Type  | Description |
|-------|------|-------------|
| [board](board/_module.md) | package | The module system encompasses full-stack functionalities of the federated learning platform, including file system management, session state maintenance, Spring Bean configuration, data persistence, API services, scheduled tasks, exception handling, and componentized machine learning workflows. Core modules provide file lifecycle management, RESTful interfaces, JPA data operations, and distributed communication protocols, supporting both horizontal and vertical federated learning scenarios. Adopting a layered design, it integrates technologies such as Spring, gRPC, and cryptographic libraries to enable end-to-end collaborative workflows from data preprocessing to model training. |


