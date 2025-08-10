# 基础信息

|      |      |
|------|------|
| 名称 | api |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/api |
| 包名 | docs.board.board-service.src.main.java.com.welab.wefe.board.service.api |
| 概述说明 | GenerateRsaKeyPairApi生成RSA密钥对返回公钥。全局配置模块提供配置更新和查询功能。账户管理模块处理会员信息查询和UI配置更新。在线演示模块支持URL生成和账号校验。数据资源模块管理多模态数据生命周期。聊天系统模块提供消息收发和状态更新。消息模块支持消息CRUD操作。服务状态模块检查版本和可用性。黑名单模块管理成员增删查。合作方配置模块处理CRUD操作。文件模块实现上传合并及安全检查。网关模块提供连接检查和任务查询。模型输出模块处理模型推送和文件导出。联盟模块管理数据资源和成员认证。日志模块查询操作记录。联邦学习模块管理项目全生命周期。数据源模块提供CRUD和连接测试。成员模块管理联盟成员信息。推理模块支持模型推理全流程。组件模块获取过滤后的组件列表。 |

# 说明

## 概述  
该模块体系核心职责是构建联邦学习平台的后端服务矩阵，涵盖数据治理（密钥生成/资源管理）、成员协作（账户/认证）、任务编排（项目/流程）和系统运维（配置/监控）四大领域，类似分布式系统的控制平面。接口规范统一采用RESTful风格，分层继承AbstractApi基类，路径按功能域划分（如`crypto/`、`project/`），输入输出均通过嵌套类结构化。关键数据结构包括三类模型：校验类（如带`@Check`注解的Input）、分页类（如PagingOutput）和业务实体类（如AccountOutputModel）。外部依赖集中为各领域Service层（如GlobalConfigService）和基础设施组件（如AES/RSA加密库）。例如GenerateRsaKeyPairApi通过TempRsaCache管理密钥，DataResourceDetailApi返回JSONObject资源详情。

## 主要业务场景  
模块支持联邦学习全链路场景：1)安全初始化（RSA密钥生成→成员认证→网关连接测试）；2)协作建模（创建项目→添加数据集→流程编排→推理服务化）；3)系统运维（配置热更新→日志审计→文件分片上传）。交互模式混合同步API调用（如CRUD操作）和异步流程（如ModelExportToFileApi），类似工作流引擎驱动。典型应用包括：密钥管理中心（GenerateRsaKeyPairApi）、成员管理后台（QueryMemberAccountsApi）、建模监控台（GetProgressApi）和风险控制模块（BlacklistMemberApi）。功能完整性体现在跨模块联动，例如项目删除触发数据清理，模型导出同步推送密钥至Serving系统。


### 包内部结构视图

```mermaid
graph TD
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
```

该流程图展示了WeFe项目的API模块层级结构，从根目录api开始，逐级展开到各个子模块如data_resource、project、member等，最终细化到具体的API实现类。图中清晰呈现了模块间的从属关系，例如project模块下包含modeling、job、dataset等多个子模块，每个子模块又包含具体的API类。整个结构层次分明，完整覆盖了所有给定的路径信息。

# 文件列表

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| [crypto](crypto/_module.md) | package | 生成RSA密钥对的API，返回公钥用于数据加密传输。 |
| [project](project/_module.md) | package | 模块提供建模信息查询API，支持分页和详情获取。任务管理模块实现全生命周期控制，包括创建、暂停、恢复等。数据集模块管理CRUD操作及审核流程。项目管理模块涵盖CRUD、状态变更及统计分析。流程管理模块处理流程编排与状态控制。成员管理模块处理增删改查及审核。联邦学习模块管理对齐任务和数据融合。节点模块负责节点信息维护和合规检查。 |
| [datasource](datasource/_module.md) | package | QueryApi用于分页查询数据源，输入包含名称和分页参数，输出为数据源详情。DeleteApi通过ID删除数据源。AddApi添加数据源，校验输入字段。TestDBConnectApi测试数据库连接，返回布尔结果。均继承基础API类，通过DataSourceService处理请求。 |
| [dev](dev/_module.md) | package | 这是一个名为ShowConfigApi的API类，路径为dev/show_config，用于生成测试数据集。它继承自AbstractNoneInputApi，返回Config对象。通过handle方法获取配置并返回成功结果。 |
| [member](member/_module.md) | package | SyncMemberToServingApi同步会员信息到服务端。IsInitializedApi检查系统初始化状态。ResetRsaKeyApi重置RSA密钥。SyncMemberToUnionApi同步会员到联盟。CheckMemberRouteConnectApi检查会员路由连接。GetMemberMachineLearningEnvApi获取会员机器学习环境。UpdateMemberInfoApi更新会员信息。UpdateMemberLogoApi更新会员logo。MemberAvailableCheckApi检查会员服务可用性。InitializeApi初始化系统。MemberDetailApi获取会员详情。 |
| [component](component/_module.md) | package | ListApi接口根据输入条件过滤组件列表，排除深度学习、未开发及已移除组件，返回符合条件的组件信息。输入参数为联邦学习类型。 |
| [model](model/_module.md) | package | 定义了6个深度学习API：下载推理结果、批量推理zip、启动推理、下载推理图片、下载模型、中止推理。均需taskId参数，处理文件操作与任务校验。 |
| [operation](operation/_module.md) | package | LogQueryApi提供分页查询操作日志功能，输入包含接口名、操作员ID和时间范围，输出操作日志分页结果。 |
| [union](union/_module.md) | package | 数据资源管理模块提供标签查询、资源检索和详情服务，采用统一接口规范。成员认证模块处理认证流程，包括文件上传和实名认证。MemberListApi查询联盟成员，GetMemberMapApi获取成员列表。AbstractThroughUnionApi是基础抽象类，封装API调用逻辑。 |
| [data_output_info](data_output_info/_module.md) | package | PushModelToServingByProviderApi推送模型到服务系统。ModelExportToFileApi导出模型文件并加密。PushRsaKeyToServingApi推送RSA密钥。ModelExportController处理模型导出请求。PushModelToServingApi同步模型到服务端。 |
| [gateway](gateway/_module.md) | package | TestConnectApi检查网关与电路板连接性。GetMemberJobProgressApi获取任务进度。GetDerivedDataSetDetailApi获取派生数据集详情。RedirectApi重定向网关请求到内部API并补充日志。 |
| [file](file/_module.md) | package | 该模块提供多格式文件安全检查，支持CSV/Excel/图片等10种类型，采用先格式校验后内容扫描流程。包含文件上传分片处理和合并功能，涉及安全检查、异常处理和目录操作。关键类包括FileUploadApi和MergeApi。 |
| [partner_config](partner_config/_module.md) | package | QueryApi实现分页查询合作方配置，Input含memberIdList和gatewayAddress，返回分页结果。DeleteApi处理删除操作，需传入id。AddApi用于添加记录，需memberId和gatewayAddress，返回生成id。均继承AbstractApi，通过PartnerConfigService执行业务逻辑。 |
| [blacklist](blacklist/_module.md) | package | BlacklistApi分页查询黑名单，路径blacklist/list。BlacklistMemberApi查询黑名单成员，路径blacklist/member。DeleteApi移除黑名单成员，路径blacklist/delete。AddApi添加成员到黑名单，路径blacklist/add。均继承基类，通过BlacklistService处理逻辑。 |
| [service](service/_module.md) | package | VersionApi提供版本信息，路径"service/version"，返回版本号、构建号和日期。ServiceAvailableApi检查服务可用性，路径"service/available"，需指定服务类型。AliveApi用于存活检测，路径"service/alive"，直接返回成功状态。 |
| [message](message/_module.md) | package | QueryApi用于分页查询消息，含多种筛选条件。ReadApi将消息标记为已读，需传入消息ID。DetailApi获取消息详情，根据ID查询并返回详情数据。 |
| [chat](chat/_module.md) | package | 定义了多个聊天相关API：查询最近账户、添加最近账户、发送消息、更新已读状态、查询聊天详情、未读消息加1、重发消息、删除最近账户。各API包含必要输入参数，通过对应服务处理请求，返回结果或空输出。 |
| [storage](storage/_module.md) | package | 预览数据集的API类，通过ID查询数据集并返回列名和数据行。支持原生和派生数据集，派生数据从流服务获取。输入为数据集ID，输出包含表头和JSON格式的数据列表。 |
| [data_resource](data_resource/_module.md) | package | 管理数据集生命周期，包括增删改查、预览及元数据操作。支持文件上传、结构化存储和样本查看。提供布隆过滤器管理、图像数据集维护及标签查询功能。接口遵循RESTful规范，统一继承AbstractApi，路径前缀明确。关键数据结构包含输入输出模型，依赖服务层处理业务逻辑。 |
| [online_demo](online_demo/_module.md) | package | TianmiantechPageApi生成天眠科技网站URL，含校验和签名。CheckAccountExistApi检查账号是否存在，输入手机号返回布尔值。TianmiantechCallApi调用天眠科技服务接口，返回JObject结果。CreateOnlineDemoAccountApi创建体验账号，无需登录。 |
| [account](account/_module.md) | package | QueryMemberAccountsApi通过会员ID查询账户信息。QueryOnlineApi查询在线账户。ListAllApi获取全量用户列表。UpdateUiConfigApi修改用户UI配置。SsoLoginApi处理单点登录请求。 |
| [global_config](global_config/_module.md) | package | GlobalConfigUpdateApi用于更新系统配置，路径global_config/update，接收必填Map类型groups字段。GetGlobalConfigApi用于获取配置，路径global_config/get，接收必填groups列表，返回配置数据Map。两者均依赖GlobalConfigService实现功能。 |


