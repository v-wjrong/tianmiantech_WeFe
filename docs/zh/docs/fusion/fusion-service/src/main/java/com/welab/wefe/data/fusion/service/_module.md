# 基础信息

|      |      |
|------|------|
| 名称 | service |
| 编码语言 | .java |
| 代码路径 | WeFe/fusion/fusion-service/src/main/java/com/welab/wefe/data/fusion/service |
| 包名 | docs.fusion.fusion-service.src.main.java.com.welab.wefe.data.fusion.service |
| 概述说明 | 联邦学习平台核心系统，含控制、数据、任务模块，支持初始化、数据管理、任务调度全流程。分层架构设计，统一接口规范，关键数据结构和多服务组件集成。 |

# 说明

## 概述  
该模块是联邦学习平台的核心管理系统，采用分层架构设计，集成系统控制、数据管理、任务调度和隐私计算功能。核心职责包括：1)通过分层存储系统（MySQL/MergeTree）实现数据持久化；2)基于PSI（隐私集合求交）算法保障跨机构数据安全对齐；3)提供全生命周期管理工具集（布隆过滤器/主键生成等）。接口规范统一采用JPA注解和RESTful风格，例如AbstractApi基类派生各类API，@Query实现扩展查询。关键数据结构涵盖分页结果集、加密业务实体（如GlobalConfigMysqlModel）和PSI执行参数（e/N/d）。外部依赖包括Spring Data JPA、RSA加密组件、连接池管理（如HikariCP）和多种数据库驱动（MySQL/Hive/Impala）。

## 主要业务场景  
模块支持联邦学习全流程管理，典型工作流为：1)系统初始化（生成RSA密钥/校验memberName）；2)数据准备（DatasetApi管理CSV/Excel解析）；3)安全计算（PsiClientActuator执行加密分片）；4)结果回调（TaskResultManager动态建表存储）。交互模式融合生产者-消费者模型（批量处理10,000行数据）和状态机驱动（TaskStatus管理7种状态）。功能完整性体现在：加密校验（≤5字段组合）、线程安全操作（ConcurrentHashMap管理任务）和异常处理链（StatusCodeWithException）。集成案例覆盖从基础配置（DataSourceConfig多数据源）到复杂业务（RSA-PSI算法切换），类似分布式ETL控制台。


### 包内部结构视图

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

该流程图展示了WeFe数据融合服务的完整项目结构，包含13个主要模块和数百个子模块。核心模块包括api接口层、service服务层、database数据层和utils工具层等，形成清晰的层级关系。api模块下细分了system、account等10个子模块，每个子模块包含多个具体API实现类；service模块实现了业务逻辑，包含bloomfilter等核心服务；database模块管理数据持久化，包含repository和entity等子模块。整体结构层次分明，模块职责单一，符合现代化微服务架构设计原则。

# 文件列表

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| [scheduled](scheduled/_module.md) | package | AccountScheduledService定时任务类，每10分钟执行一次，自动禁用90天未活跃账户和注销180天未活跃账户，并记录日志。 |
| [operation](operation/_module.md) | package | FusionApiLogger继承AbstractApiLogger，忽略特定API日志，保存日志到数据库并更新账户最后操作时间。 |
| [listener](listener/_module.md) | package | 自动数据库加密监听器，在应用启动时检查配置并执行加密服务，记录操作日志和异常。 |
| [FusionService.java](FusionService.md) | file | SpringBoot应用集成调度与异步任务，自定义组件扫描路径，实现API权限校验及RSA签名验证，通过Launcher启动并管理应用上下文。 |
| [config](config/_module.md) | package | Config类继承CommonConfig，通过@PropertySource加载外部配置文件，包含短信验证码发送渠道、阿里云短信配置、服务器IP等属性，提供getter/setter方法。 |
| [task](task/_module.md) | package | PsiClientTask继承AbstractPsiTask，处理PSI客户端任务。AbstractTask是管理任务流程的抽象类。PsiServerTask继承AbstractPsiTask，处理PSI服务器任务。AbstractPsiTask是处理PSI执行器任务的抽象基类。 |
| [dto](dto/_module.md) | package | 账户模块处理数据校验与脱敏，联邦学习模块管理数据与任务，分页模块封装分页查询功能。 |
| [service](service/_module.md) | package | 布隆过滤器管理模块负责创建、更新、查询及监控，支持多线程和加密校验。全局配置模块管理成员信息和邮件设置，支持分组操作。数据集模块处理创建、状态跟踪和批量处理。任务服务管理任务状态、统计和请求处理。系统初始化服务检查并初始化系统配置。合作伙伴服务管理合作伙伴数据。存储服务提供数据库操作功能。单点登录服务处理账户初始化和更新。抽象服务提供日志功能。数据存储服务管理表操作。字段信息服务处理字段列名和属性。任务结果服务管理结果表。回调服务处理任务回调。缓存工具类管理静态数据。隐私数据加密服务处理数据库加密。数据源服务管理数据源连接和验证。表头服务获取数据集表头。第三方服务处理合作方交互。操作日志服务查询日志记录。 |
| [manager](manager/_module.md) | package | TaskResultManager管理任务结果数据，支持建表、插入和批量保存。ActuatorManager管理任务执行器，提供线程安全的任务和布隆过滤器操作。JdbcManager是已弃用的JDBC工具类，支持多种数据库连接和查询。 |
| [actuator](actuator/_module.md) | package | PsiClientActuator和PsiServerActuator构成PSI双端模块，采用RSA加密和布隆过滤器实现安全数据对齐。客户端加密比对，服务端处理请求，支持跨机构数据匹配如金融风控。AbstractActuator是抽象类，含初始化、处理和入库方法，使用LongAdder计数。 |
| [enums](enums/_module.md) | package | 定义了多个枚举类型：RoleType（promoter/provider）、DBType（6种数据库）、Options（4种处理方式）、TaskStatus（7种任务状态）、DataResourceType（2种资源类型）、DataResourceSource（3种来源）、AlgorithmType（2种算法）、CallbackType（4种回调状态）、Progress（6种进度）、ActionType（5种操作）、PSIActuatorRole（2种角色）、PSIActuatorStatus（6种状态）。 |
| [utils](utils/_module.md) | package | 布隆过滤器实现高性能数据去重，主键生成模块支持多种哈希算法，数据解析工具处理CSV/Excel/DB数据源，去重模块提供布隆过滤器和内存集合两种策略，文件类型检查器限制xls/xlsx/csv格式，Socket工具管理连接重试，字节工具类实现整型与字节数组转换。 |
| [database](database/_module.md) | package | 基于Spring Data JPA的通用仓库框架，提供标准化数据访问和原生SQL扩展，支持多实体CRUD、事务操作及复杂查询。包含MySqlModel系列实体，依赖Spring Data JPA和Hibernate。用于数据融合服务，涵盖任务管理、数据集处理等全生命周期。配置类DataSourceConfig设置数据源和JPA参数。 |
| [repo](repo/_module.md) | package | MysqlStorage继承AbstractStorage，实现MySQL操作：建表、删表、插入、批量插入和计数，含异常处理和连接池管理。Storage定义存储抽象方法，AbstractStorage扩展功能并实现资源管理。 |
| [api](api/_module.md) | package | 系统管理模块负责初始化、配置和密钥管理；合作伙伴模块提供增删改查功能；布隆过滤器模块支持CRUD和状态查询；第三方服务模块处理回调和状态检测；文件模块管理分片上传与合并；数据集模块实现生命周期管理；日志模块查询操作记录；任务模块管理任务全周期；数据源模块处理数据源CRUD和连接测试。 |


