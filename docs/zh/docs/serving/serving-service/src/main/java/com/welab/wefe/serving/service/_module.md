# 基础信息

|      |      |
|------|------|
| 名称 | service |
| 编码语言 | .java |
| 代码路径 | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service |
| 包名 | docs.serving.serving-service.src.main.java.com.welab.wefe.serving.service |
| 概述说明 | Config类：Spring组件，加载外部配置，定义文件路径、邮件主题等属性，支持UTF-8编码。XxxModelProcessor类：继承抽象类，空实现预处理和后处理方法。联邦学习核心API：提供加密通信、成员管理等功能，RESTful设计。预测引擎：支持联合预测，含标准、批量、调试模式。ORM层：JPA实现数据管理，含20+实体类。工具集：签名验证、加密等。枚举模块：定义服务状态和类型。隐私计算框架：处理PSI/PIR/SA请求。特征管理：统一管理数据源和模型。服务治理：全局配置和模型生命周期管理。定时任务：执行统计和状态维护。DTO管理：封装业务数据交互。日志处理：记录API日志到MySQL。启动监听器：执行初始化任务。特征处理框架：注解和SQL驱动。ServingService主类：Spring Boot应用启动配置。 |

# 说明

## 概述  
该模块是联邦学习服务系统的核心组件集合，采用微服务架构设计，核心职责包括系统配置管理、联合预测执行、数据持久化和安全通信。接口规范分层统一：配置类采用Spring属性注入（如Config），处理器类遵循模板方法模式（如XxxModelProcessor），API层继承AbstractApi基类实现RESTful交互。关键数据结构聚合为四类：系统配置（如PSI批量大小）、预测参数（如FederatedPredictParam）、持久化模型（如PredictLogMySqlModel）和枚举状态（如ServiceTypeEnum）。外部依赖去重后包含Spring生态（JPA/Cloud）、加密组件（SM2/RSA）、多数据库驱动（MySQL/Doris/Hive）及JNI调用。例如Config管理SM2密钥，PromoterPredictor协调多方预测。  

## 主要业务场景  
模块支撑联邦学习全生命周期管理，业务流程整合为：1) 系统初始化（密钥生成→配置加载→服务注册）；2) 联合预测（特征获取→安全计算→结果聚合）；3) 服务治理（日志统计→费用结算→状态跟踪）。典型交互模式类似主从架构，通过PromoterPredictor协调多节点计算，依赖签名验证框架保障通信安全。功能完整性体现在：配置中心（Config）、预测引擎（Predicter）、持久化层（Database）和服务治理（Service）的协同。例如金融风控场景中，银行通过InitializeApi初始化→调用PromoterPredictor→记录PredictLogMySqlModel→生成FeeDetailMysqlModel。API类型覆盖加密通信、成员管理、模型预测和定时任务，集成案例可见于ServingService的启动流程（加载处理器→初始化监听器→启动API服务）。


### 包内部结构视图

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

该流程图展示了WeFe/serving项目的完整目录结构，从顶层service节点开始，逐级展开所有子模块和文件。主要包含api接口、数据库操作、工具类、枚举定义、服务处理器、管理模块、定时任务等核心组件。每个模块都按照实际路径关系进行组织，清晰呈现了项目代码的组织架构和依赖关系，便于开发者快速理解系统设计。

# 文件列表

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| [config](config/_module.md) | package | Java配置类，包含文件路径、邮件主题内容、PSI批次大小及密钥类型等属性，支持外部配置注入和默认值设置。 |
| [predicter](predicter/_module.md) | package | 该模块提供联邦学习预测功能，支持标准/调试模式，含单用户/批量预测、协作方API调用及特征获取。关键类包括Predictor、PromoterPredictHelper等，依赖模型和特征管理服务。适用于金融风控等多方数据协作场景。 |
| [listener](listener/_module.md) | package | AutoPrivacyDatabaseEncryptListener是Spring组件，监听启动事件，自动检查并执行数据库加密，记录日志。ApplicationStartedListener监听启动，初始化缓存，统计订单数据，保存费用明细，处理异常并记录日志。 |
| [api](api/_module.md) | package | GenerateRsaKeyPairApi生成RSA密钥对并返回公钥。客户端管理模块支持CRUD操作，校验IP和公钥。系统模块管理全局配置和密钥。账户模块处理SSO登录和查询。订单统计模块提供查询、下载和保存功能。合作伙伴模块管理增删改查。API记录模块支持查询和下载。安全聚合模块处理聚合结果。预测模块提供模型预测服务。计费模块管理配置。服务订单模块处理订单管理。客户端服务模块管理服务生命周期。支付记录模块支持查询和下载。日志模块提供统计和查询。文件模块支持分块上传和合并。费用明细模块查询费用。PIR模块提供私有信息检索。数据源模块管理数据库连接。成员模块管理联邦成员。模型模块管理模型生命周期。SaveMemberApi保存成员信息。 |
| [service](service/_module.md) | package | 管理系统全局配置初始化和维护，支持多模式初始化和安全更新。包含初始化检查、独立/联合模式初始化及配置更新等方法。关键数据结构涉及AbstractConfigModel基类和加密字段。依赖RSA密钥管理和数据库存储层。 |
| [operation](operation/_module.md) | package | ServingApiLogger继承AbstractApiLogger，忽略特定API日志记录，保存操作日志到数据库并更新账户最后操作时间。 |
| [ServingService.java](ServingService.md) | file | 这是一个Spring Boot应用启动类，排除了数据源自动配置，启用了定时任务，自定义了组件扫描命名规则。主方法通过Launcher启动，配置了API权限验证逻辑，并初始化了模型和特征处理器。同时实现了应用上下文注入功能。 |
| [feature](feature/_module.md) | package | 特征处理框架提供单条/批量模式，含抽象类与注解注册机制，支持空处理及扩展。数据库模块封装多库JDBC操作，含连接池管理与SQL校验。SqlFeatureDataHandler实现多库查询，CodeFeatureDataHandler通过反射管理处理器映射。 |
| [dto](dto/_module.md) | package | 注解驱动全局配置管理模块，自动收集分类配置模型，支持分组检索。包含多个DTO类如ServiceOrderInput、TreeNode等，用于处理服务订单、树形结构、模型状态等数据。提供分页、日志、成员参数管理功能。 |
| [scheduler](scheduler/_module.md) | package | LogStatisticsScheduler记录统计信息，初始延迟5秒，固定延迟120秒。AccountScheduledService每10分钟处理不活跃账户，首次延迟10秒。OrderStatisticsScheduler每分钟统计订单数据。PredictScoreStatisticsScheduler每5分钟刷新预测分数统计。OrderToFeeDetailScheduler每小时处理费用记录。 |
| [manager](manager/_module.md) | package | FeatureManager管理特征数据，缓存数据源，线程安全。JdbcManager已过时，支持多数据库连接和操作。ModelManager管理模型状态，提供缓存和同步方法。 |
| [service_processor](service_processor/_module.md) | package | SAQueryServiceProcessor处理安全聚合查询，使用DH密钥交换；MultiPsiServiceProcessor处理多客户端PSI查询；ServiceProcessorUtils维护服务类型映射；PirServiceProcessor处理私有信息检索；PsiServiceProcessor实现PSI服务核心功能；ModelServiceProcessor处理模型预测；MultiPirServiceProcessor处理多PIR请求；AbstractServiceProcessor是抽象基类；SAServiceProcessor执行SQL查询并缓存结果。 |
| [enums](enums/_module.md) | package | DataResourceSource枚举定义数据来源类型：本地文件、上传文件、数据库。ServiceTypeEnum枚举定义八种服务类型，含查询统计和模型服务。MemberModelStatusEnum枚举成员模型状态：离线、不可用、可用。DateTypeEnum枚举四种日期粒度：月、日、小时、分钟。ServiceOrderEnum枚举三种订单状态：成功、失败、进行中。CallByMeEnum枚举是否调用：是、否。ModelTypeEnum枚举模型类型：机器学习、深度学习。ServiceResultEnum枚举六种服务结果状态码。PaymentsRecordStatusEnum枚举支付状态：正常、冲正。PayTypeEnum枚举两种支付类型：后付费、预付费。QueryDateTypeEnum枚举四种日期查询类型。ServingModeEnum枚举服务模式：独立、联合。ServiceClientTypeEnum枚举客户端类型：激活、开通。ServiceStatusEnum枚举服务状态：启用、未启用。ClientStatusEnum枚举客户端状态：正常、删除。ServiceCallStatusEnum枚举五种调用状态。PaymentsTypeEnum枚举支付类型：充值、支出。 |
| [utils](utils/_module.md) | package | 可扩展签名验证框架，支持多种策略模式，涵盖RSA验签、身份核验等功能。包含加密工具类（SHA256、MD5）、序列化、Redis缓存操作、文件处理及深度学习服务调用等实用工具。 |
| [database](database/_module.md) | package | 基于Spring Data JPA的增强仓储层，提供统一数据访问、审计追踪、动态字段更新及SQL查询转换。支持复杂查询、多表关联和跨库聚合，适用于金融级数据服务。联邦学习服务的数据持久化层，通过JPA实体映射实现ORM操作，涵盖全生命周期数据管理。配置类支持多数据源环境，定义主数据源、实体扫描路径和事务管理。 |
| [processor](processor/_module.md) | package | 这是一个名为XxxModelProcessor的模型处理器类，继承自AbstractModelProcessor，包含预处理preprocess和后处理postprocess方法，用于处理模型预测前后的逻辑。 |


