# 基础信息

|      |      |
|------|------|
| 名称 | wefe |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe |
| 包名 | docs.board.board-service.src.main.java.com.welab.wefe |
| 概述说明 | 该模块体系涵盖联邦学习平台全栈功能，包括文件系统管理、会话状态维护、Spring Bean配置、数据持久化、API服务、定时任务、异常处理及组件化机器学习流程。核心模块提供文件生命周期管理、RESTful接口、JPA数据操作及分布式通信协议，支持横向/纵向联邦学习场景。采用分层设计，集成Spring、gRPC、加密库等技术，实现从数据预处理到模型训练的全流程协同。 |

# 说明

## 概述  
该模块是联邦学习平台的核心服务矩阵，整合文件系统管理、会话状态维护、Spring容器配置、数据持久化及分布式通信等能力，类似企业级AI协作中枢。统一接口规范涵盖RESTful API（分层继承AbstractApi）、JPA标准（BaseRepository扩展）及Protobuf/gRPC协议（TransferServiceGrpc）。关键数据结构形成多维度体系：业务实体类（JobMySqlModel）、校验模型（带@Check注解的Input）、枚举常量（ServiceStatus）及传输元数据（TransferMeta分片单元）。外部依赖集中于Spring生态（JPA/WebSocket）、加密组件（RSA/AES）、机器学习框架（PaddlePaddle/XGBoost）及存储系统（MySQL/LMDB）。例如DownloadDeepLearningModel处理模型文件，GenerateRsaKeyPairApi管理密钥生命周期。

## 主要业务场景  
模块支持联邦学习全链路场景：1)安全初始化（RSA密钥生成→CA证书缓存刷新→网关连接测试）；2)协作建模（数据分片去重→PSI样本对齐→横向逻辑回归训练）；3)系统运维（定时清理闲置账户→配置热更新→文件分片上传）。交互模式融合同步CRUD（如AccountService）、异步流程（ModelExportService）和事件驱动（ApplicationListener），类似工作流引擎与消息总线结合体。典型应用包括跨机构数据融合（布隆过滤器去重）、流程图节点管理（BaseFlowGraph防循环依赖）及实时通信（WebSocket双工会话）。功能完整性体现在多组件联动，例如项目删除触发级联清理，模型导出同步推送密钥至Serving系统。


### 包内部结构视图

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

该流程图展示了WeFe/board/board-service项目的完整模块结构，包含15个一级模块和超过100个二级模块。核心模块包括service（业务服务）、database（数据库相关）、component（组件系统）和dto（数据传输对象）。service模块进一步细分为account、data_resource等23个子服务，database模块包含repository和entity两大分支。组件系统采用分层设计，包含建模、深度学习、特征工程等专业组件。整体架构呈现清晰的层级关系，模块间通过明确定义的接口进行交互，体现了复杂业务系统的模块化设计思想。

# 文件列表

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| [board](board/_module.md) | package | 该模块体系涵盖联邦学习平台全栈功能，包括文件系统管理、会话状态维护、Spring Bean配置、数据持久化、API服务、定时任务、异常处理及组件化机器学习流程。核心模块提供文件生命周期管理、RESTful接口、JPA数据操作及分布式通信协议，支持横向/纵向联邦学习场景。采用分层设计，集成Spring、gRPC、加密库等技术，实现从数据预处理到模型训练的全流程协同。 |


