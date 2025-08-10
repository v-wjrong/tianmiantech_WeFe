# 基础信息

|      |      |
|------|------|
| 名称 | service |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service |
| 包名 | docs.board.board-service.src.main.java.com.welab.wefe.board.service |
| 概述说明 | 该模块体系涵盖联邦学习平台全栈功能，包括文件系统管理、会话状态维护、Spring Bean配置、数据持久化、API服务、定时任务、异常处理及组件化机器学习流程。核心模块提供文件生命周期管理、RESTful接口、JPA数据操作及分布式通信协议，支持横向/纵向联邦学习场景。采用分层设计，集成Spring、gRPC、加密库等技术，实现从数据预处理到模型训练的全流程协同。 |

# 说明

## 概述  
该模块是联邦学习平台的核心服务矩阵，整合文件系统管理、会话状态维护、Spring容器配置、数据持久化及分布式通信等能力，类似企业级AI协作中枢。统一接口规范涵盖RESTful API（分层继承AbstractApi）、JPA标准（BaseRepository扩展）及Protobuf/gRPC协议（TransferServiceGrpc）。关键数据结构形成多维度体系：业务实体类（JobMySqlModel）、校验模型（带@Check注解的Input）、枚举常量（ServiceStatus）及传输元数据（TransferMeta分片单元）。外部依赖集中于Spring生态（JPA/WebSocket）、加密组件（RSA/AES）、机器学习框架（PaddlePaddle/XGBoost）及存储系统（MySQL/LMDB）。例如DownloadDeepLearningModel处理模型文件，GenerateRsaKeyPairApi管理密钥生命周期。

## 主要业务场景  
模块支持联邦学习全链路场景：1)安全初始化（RSA密钥生成→CA证书缓存刷新→网关连接测试）；2)协作建模（数据分片去重→PSI样本对齐→横向逻辑回归训练）；3)系统运维（定时清理闲置账户→配置热更新→文件分片上传）。交互模式融合同步CRUD（如AccountService）、异步流程（ModelExportService）和事件驱动（ApplicationListener），类似工作流引擎与消息总线结合体。典型应用包括跨机构数据融合（布隆过滤器去重）、流程图节点管理（BaseFlowGraph防循环依赖）及实时通信（WebSocket双工会话）。功能完整性体现在多组件联动，例如项目删除触发级联清理，模型导出同步推送密钥至Serving系统。


### 包内部结构视图

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

# 文件列表

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| [dto](dto/_module.md) | package | 模块统一管理多类型业务实体生命周期，含数据资源、消息、标注和任务处理。支持联邦学习全流程，包括任务配置、成员拓扑管理、数据融合及分页查询。采用分层设计，依赖多种框架，实现标准化接口与状态驱动交互。 |
| [component](component/_module.md) | package | 联邦学习平台组件集合，包含数据交互、特征工程、机器学习建模（逻辑回归/XGBoost/神经网络）、深度学习（PaddlePaddle图像处理）、评估验证等模块。采用策略模式设计，支持横向/纵向/混合场景，统一接口规范（参数校验-JSON配置-结果输出），依赖Java标准库和内部服务。 |
| [BoardService.java](BoardService.md) | file | BoardService是SpringBoot应用入口，集成定时和异步任务，自定义组件扫描和权限控制，处理API异常和流量限制，支持RSA签名验证。 |
| [service](service/_module.md) | package | AccountService提供账户管理功能，依赖多个服务，支持查询、筛选、登录等操作。GlobalConfigService管理全局配置，确保安全性和一致性。ProjectService管理项目全生命周期，包括成员、数据集和状态。GatewayService处理消息同步和网关通信。DataResourceService统一管理各类数据集CRUD操作。Fusion模块处理数据融合任务生命周期。ModelExport实现多语言模型代码生成。Checkpoint模块检查服务健康状态。其他服务包括消息、聊天、任务、证书等管理功能。 |
| [fusion](fusion/_module.md) | package | 枚举定义导出状态：失败、成功、进行中。模块实现PSI任务处理，含数据转储、状态同步和线程安全，依赖多项服务。管理执行器状态和导出进度，采用缓存优先策略，支持任务防重和进度查询。 |
| [model](model/_module.md) | package | JobBuilder类含dataSetVersion字段标记图像数据集版本，优化下载性能。BaseFlowGraph是管理联邦学习流程图的抽象基类，含任务、节点等核心属性和方法。FlowGraph继承BaseFlowGraph，支持多种初始化及节点查找功能。FlowGraphNode表示流程图节点，含深度、父子节点等属性及任务生成方法。 |
| [listener](listener/_module.md) | package | AppListener监听环境准备事件并记录日志。ApplicationStartedListener处理应用启动，初始化配置、加密数据库、加载证书等。ApplicationReadyListener在启动完成后管理网关白名单和清理任务。 |
| [operation](operation/_module.md) | package | BoardApiLogger继承AbstractApiLogger，忽略特定API日志记录，保存操作日志到数据库并更新账户最后操作时间。 |
| [cache](cache/_module.md) | package | CaCertificateCache类是一个单例模式的CA证书缓存，使用ConcurrentHashMap存储证书数据，提供刷新缓存、获取单个或全部证书的功能。内部类CaCertificate包含id、name和content属性。 |
| [onlinedemo](onlinedemo/_module.md) | package | 天眠科技服务类继承抽象类，含URL和RSA密钥配置，提供through和request方法处理签名请求。OnlineDemoBranchStrategy的hackOnDelete方法在线演示时校验用户权限，仅允许创建者删除数据。 |
| [scheduled](scheduled/_module.md) | package | AccountScheduledService定时管理账户，每小时执行禁用90天和注销180天无活动账户。OnlineDemoScheduledService每10分钟清理演示环境数据，包括项目及日志。CaCertificateScheduledService每30秒刷新CA证书缓存。 |
| [exception](exception/_module.md) | package | MemberGatewayException是处理成员网关错误的异常类，含成员ID字段，构造函数初始化ID和错误信息，默认状态码REMOTE_SERVICE_ERROR，重写getMessage返回格式化信息。FlowNodeException表示流程图节点异常，含FlowGraphNode字段，构造函数初始化节点和异常信息，重写getMessage返回格式化消息，提供getNode方法。 |
| [proto](proto/_module.md) | package | 分布式通信与存储元数据协议，含端点管理、状态机、存储定位器。基于Protobuf，支持异步事件驱动，用于跨节点路由和异构存储访问。含gRPC服务接口。 |
| [util](util/_module.md) | package | 模块1管理字段元数据并生成主键，含FieldInfo和PrimaryKeyUtils类，支持哈希处理。模块2提供数据集去重功能，含布隆过滤器和内存HashSet两种策略。多个Reader类（Excel、CSV、SQL）继承抽象类读取数据，支持表头处理、行数统计和资源释放。TlsUtil类转换证书格式。 |
| [constant](constant/_module.md) | package | Config类继承CommonConfig，加载动态路径配置文件，支持多环境。BloomfilterAddMethod枚举定义HTTP上传、本地文件、数据库三种数据添加方式。ServiceStatus枚举包含正常和离线状态及描述。ChatConstant类提供聊天消息方向、状态及键值常量。DataSetAddMethod枚举定义三种数据集添加方式。 |
| [sdk](sdk/_module.md) | package | 管理成员基础信息与联盟数据服务，包含MemberBaseInfo数据结构和UnionService服务类。支持成员状态管理、数据资源共享、权限检查及异步缓存。依赖Java库及缓存框架。 |
| [database](database/_module.md) | package | 基于Spring Data JPA的通用数据访问层，统一管理业务实体持久化，支持CRUD、批量更新和分页。关键数据结构含40+实体类，依赖Spring Data JPA保障事务安全。支撑全业务生命周期管理，涵盖数据预处理、任务调度等场景。 |
| [api](api/_module.md) | package | GenerateRsaKeyPairApi生成RSA密钥对返回公钥。全局配置模块提供配置更新和查询功能。账户管理模块处理会员信息查询和UI配置更新。在线演示模块支持URL生成和账号校验。数据资源模块管理多模态数据生命周期。聊天系统模块提供消息收发和状态更新。消息模块支持消息CRUD操作。服务状态模块检查版本和可用性。黑名单模块管理成员增删查。合作方配置模块处理CRUD操作。文件模块实现上传合并及安全检查。网关模块提供连接检查和任务查询。模型输出模块处理模型推送和文件导出。联盟模块管理数据资源和成员认证。日志模块查询操作记录。联邦学习模块管理项目全生命周期。数据源模块提供CRUD和连接测试。成员模块管理联盟成员信息。推理模块支持模型推理全流程。组件模块获取过滤后的组件列表。 |
| [config](config/_module.md) | package | CertBeans是Java配置类，提供CertService的Bean定义。WebSocketConfig配置类注册WebSocket端点并解决依赖注入问题。 |
| [base](base/_module.md) | package | WeFeFileSystem类管理文件上传存储和目录，含UseType枚举定义文件用途，子类处理模型下载和调用。OnlineDemoApi是运行时类注解。LoginAccountInfo单例类管理登录用户信息，使用过期Map存储。 |


