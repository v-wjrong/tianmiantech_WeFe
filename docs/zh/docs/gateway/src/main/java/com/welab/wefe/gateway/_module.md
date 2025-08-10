# 基础信息

|      |      |
|------|------|
| 名称 | gateway |
| 编码语言 | .java |
| 代码路径 | WeFe/gateway/src/main/java/com/welab/wefe/gateway |
| 包名 | docs.gateway.src.main.java.com.welab.wefe.gateway |
| 概述说明 | gRPC网关系统，含服务器管理、缓存加载、安全拦截、数据传输、存储访问、定时刷新、健康检查等功能模块，支持双通道通信、动态TLS、流式处理及分布式监控。 |

# 说明

## 概述  
该模块是分布式系统的核心通信网关，集成gRPC服务管理、安全拦截、数据流式传输与缓存同步四大功能，类似微服务架构的中枢神经系统。统一接口规范涵盖服务器控制（启动/停止/TLS切换）、安全元数据构建（签名/时间戳）、流式传输协议（GatewayMetaProto）及缓存操作API（refreshCache）。关键数据结构包括GrpcServerContext、TransferMeta传输元数据、StorageLocator存储定位器及各类Cache单例（如MemberBlacklistCache）。外部依赖涉及gRPC框架、Protobuf序列化、Spring Data JPA、TLS/SSL协议及云平台服务。例如通过AntiTamperServerInterceptor实现请求防篡改，PushDataSourceRequestStreamObserver处理双向流数据。

## 主要业务场景  
模块支撑三大典型场景：1)安全通信链（IP白名单→签名验证→TLS加密→防重放），类似API网关的零信任架构；2)流式数据管道（客户端推送→存储定位→状态反馈），采用生产者-消费者模型；3)缓存热加载体系（定时刷新→异常回滚→异步处理），如每10秒同步黑名单数据。业务流程整合端口校验、服务注册、证书管理及跨节点传输，交互模式涵盖链式拦截（类似Servlet过滤器）、构建器模式（StorageLocator动态配置）和注解驱动（@GrpcServer服务注册）。典型应用包括联盟成员管理（通过UnionHelper查询CA证书）、分片存储路由（使用fragment字段）及TLS热更新（restartExternalServer触发）。API类型覆盖一元RPC、流式接口及Spring Data仓库，集成案例丰富如DatabaseEncryptUtil实现SM4字段加密，InitListener完成gRPC服务冷启动。


### 包内部结构视图

```mermaid
graph TD
    gateway --> init
    gateway --> interceptor
    gateway --> api
    gateway --> repository
    gateway --> sdk
    gateway --> util
    gateway --> common
    gateway --> service
    gateway --> entity
    gateway --> scheduler
    gateway --> cache
    gateway --> listener
    gateway --> base
    gateway --> config
    gateway --> GatewayServer.java
    init --> grpc
    init --> LoadMemberBlacklistToCache.java
    init --> LoadRecvTransferMateToCache.java
    init --> LoadSendTransferMetaToCache.java
    init --> LoadMemberToCache.java
    init --> LoadSystemConfigToCache.java
    init --> SendTransferMetaCacheTask.java
    init --> InitStorageManager.java
    grpc --> GrpcServerContext.java
    grpc --> GrpcServer.java
    interceptor --> SystemTimestampMetadataBuilder.java
    interceptor --> AntiTamperServerInterceptor.java
    interceptor --> SignVerifyServerInterceptor.java
    interceptor --> SignVerifyMetadataBuilder.java
    interceptor --> AbstractServerInterceptor.java
    interceptor --> AbstractCallCredentials.java
    interceptor --> ClientCallCredentials.java
    interceptor --> AbstractMetadataBuilder.java
    interceptor --> SystemTimestampVerifyServerInterceptor.java
    interceptor --> AntiTamperMetadataBuilder.java
    interceptor --> IpAddressWhiteListServerInterceptor.java
    api --> streammessage
    api --> meta
    api --> service
    streammessage --> PushDataSourceRequestStreamObserver.java
    streammessage --> PushDataSourceResponseStreamObserver.java
    meta --> storage
    meta --> basic
    storage --> StorageMetaProto.java
    basic --> GatewayMetaProto.java
    basic --> BasicMetaProto.java
    service --> proto
    service --> TransferGrpcServer.java
    service --> NetworkDataTransferProxyGrpcServer.java
    proto --> TransferServiceProto.java
    proto --> NetworkDataTransferProxyServiceGrpc.java
    proto --> TransferServiceGrpc.java
    repository --> CertKeyInfoRepository.java
    repository --> FlowActionQueueRepository.java
    repository --> MessageQueueRepository.java
    repository --> CertRequestInfoRepository.java
    repository --> BaseRepository.java
    repository --> MessageRepository.java
    repository --> CertInfoRepository.java
    repository --> BlacklistRepository.java
    repository --> GlobalConfigRepository.java
    repository --> PartnerConfigRepository.java
    sdk --> BoardHelper.java
    sdk --> UnionHelper.java
    util --> DatabaseEncryptConverter.java
    util --> ClassUtil.java
    util --> ReturnStatusUtil.java
    util --> TlsUtil.java
    util --> ExceptionUtil.java
    util --> SerializeUtil.java
    util --> TransferMetaUtil.java
    util --> DatabaseEncryptUtil.java
    util --> GrpcUtil.java
    common --> ReturnStatusBuilder.java
    common --> GrpcServerScopeEnum.java
    common --> GrpcConstant.java
    common --> EndpointBuilder.java
    common --> MessageEntityBuilder.java
    common --> ReturnStatusEnum.java
    common --> TransferMetaCachePersistentTypeEnum.java
    common --> RpcServerStatusEnum.java
    common --> KeyValueDataBuilder.java
    common --> StorageConstant.java
    service --> processors
    service --> base
    processors --> available
    processors --> RefreshFcStorageProcessor.java
    processors --> RefreshMemberBlacklistCacheProcessor.java
    processors --> DbFlowTableProcessor.java
    processors --> BoardHttpProcessor.java
    processors --> DbChatTableProcessor.java
    processors --> RefreshMemberCacheProcessor.java
    processors --> RefreshSystemConfigCacheProcessor.java
    processors --> ResidentMemoryProcessor.java
    processors --> RemoteCallbackProcessor.java
    processors --> AbstractProcessor.java
    processors --> RestartExternalGrpcServerProcessor.java
    processors --> RefreshPartnerConfigCacheProcessor.java
    processors --> RefreshPersistentStorageProcessor.java
    processors --> DsourceProcessor.java
    processors --> AvailableCheckBeforeStartJobProcessor.java
    processors --> ProcessorContext.java
    available --> checkpoint
    available --> GatewayAliveProcessor.java
    available --> GatewayAvailableProcessor.java
    checkpoint --> FcCheckpoint.java
    checkpoint --> MysqlCheckpoint.java
    checkpoint --> FileSystemCheckpoint.java
    checkpoint --> StorageCheckpoint.java
    checkpoint --> BoardCheckpoint.java
    checkpoint --> UnionCheckpoint.java
    base --> AbstractRecvTransferMetaCachePersistentService.java
    base --> AbstractTransferMetaDataSource.java
    base --> AbstractTransferMetaDataSink.java
    base --> AbstractSendTransferMetaService.java
    base --> AbstractSendTransferMetaCachePersistentService.java
    base --> AbstractFlowActionQueueService.java
    base --> AbstractRecvTransferMetaService.java
    base --> AbstractMemberService.java
    service --> FlowActionQueueService.java
    service --> RecvTransferMetaCachePersistentService.java
    service --> GlobalConfigService.java
    service --> AbstractService.java
    service --> MessageQueueService.java
    service --> PartnerConfigService.java
    service --> MessageService.java
    service --> ServerCertService.java
    service --> TransferMetaDataSourceStream.java
    service --> BlacklistService.java
    service --> SendTransferMetaService.java
    service --> TransferMetaDataSource.java
    service --> TransferMetaDataSourceParallelStream.java
    service --> MemberService.java
    service --> CaCertificateService.java
    service --> RecvTransferMetaService.java
    service --> TransferMetaDataAsyncSaveService.java
    service --> SendTransferMetaCachePersistentService.java
    service --> TransferMetaDataSink.java
    entity --> CertInfoEntity.java
    entity --> PartnerConfigEntity.java
    entity --> MessageEntity.java
    entity --> MemberEntity.java
    entity --> MessageQueueEntity.java
    entity --> BlacklistEntity.java
    entity --> CertKeyInfoEntity.java
    entity --> FlowActionQueueEntity.java
    entity --> FlagEntity.java
    entity --> AbstractBaseEntity.java
    entity --> CertRequestInfoEntity.java
    entity --> GlobalConfigEntity.java
    scheduler --> RefreshPartnerConfigCacheScheduler.java
    scheduler --> RefreshSystemConfigCacheScheduler.java
    scheduler --> RefreshMemberBlacklistCacheScheduler.java
    scheduler --> RefreshMemberCacheScheduler.java
    scheduler --> RefreshCaCertificateCacheScheduler.java
    cache --> RecvTransferMetaCache.java
    cache --> GrpcChannelCache.java
    cache --> PartnerConfigCache.java
    cache --> CaCertificateCache.java
    cache --> MemberCache.java
    cache --> SystemConfigCache.java
    cache --> RecvTransferMetaCountDownLatchCache.java
    cache --> MemberBlacklistCache.java
    cache --> SendTransferMetaCache.java
    listener --> InitListener.java
    base --> Processor.java
    base --> GrpcServerAnnotate.java
    base --> GrpcServer.java
    base --> ProcessorAnnotate.java
    config --> DataSourceConfig.java
    config --> ConfigProperties.java
    config --> AsyncTaskConfig.java
    config --> CommonConfig.java
```

该流程图展示了WeFe网关项目的完整目录结构，从顶层gateway节点开始，逐级展开到各个子模块和文件。项目包含14个主要模块，其中service模块最为复杂，包含processors和base两个子模块，processors下又细分available和checkpoint层级。整体结构清晰展现了网关系统的功能划分，包括初始化模块、拦截器、API服务、数据访问层、工具类和各种服务实现类。

# 文件列表

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| [base](base/_module.md) | package | Processor注解标记类，含类型和描述元素，是Spring组件。GrpcServerAnnotate管理带GrpcServer注解的服务，维护全局映射，含服务对象、范围、拦截器等属性。GrpcServer注解标记gRPC组件，含名称、范围、拦截器等配置。ProcessorAnnotate管理带Processor注解的处理器，维护全局映射，含名称、描述和处理器对象。 |
| [cache](cache/_module.md) | package | RecvTransferMetaCache管理传输元数据缓存，GrpcChannelCache管理gRPC通道，PartnerConfigCache缓存合作伙伴配置，CaCertificateCache存储CA证书，MemberCache管理成员信息，SystemConfigCache处理IP白名单，CountDownLatchCache管理锁存器，MemberBlacklistCache维护黑名单，SendTransferMetaCache管理传输数据队列。均为单例线程安全实现。 |
| [scheduler](scheduler/_module.md) | package | 五个Spring定时任务类，分别每10/30秒刷新合作伙伴配置、系统配置、会员黑名单、成员和CA证书缓存，均含开始/成功/失败日志记录。 |
| [entity](entity/_module.md) | package | CertInfoEntity存储证书内容、CSR ID和状态。PartnerConfigEntity记录成员ID和网关地址。MessageEntity管理消息生产者、级别、内容等。MemberEntity包含成员信息、网络配置和TLS状态。MessageQueueEntity处理消息队列数据。BlacklistEntity存储黑名单成员ID。CertKeyInfoEntity保存密钥PEM和算法。FlowActionQueueEntity管理动作队列。FlagEntity为空类。AbstractBaseEntity定义创建/更新信息。CertRequestInfoEntity存储证书请求详情。GlobalConfigEntity管理加密配置项。 |
| [GatewayServer.java](GatewayServer.md) | file | SpringBoot网关服务主类，启用组件扫描、定时任务和异步处理，排除数据源自动配置，提供全局应用上下文访问。 |
| [api](api/_module.md) | package | 模块1实现双向流式数据传输，处理TransferMeta数据，含请求/响应流接口，依赖异步协调机制。模块2定义Protobuf存储协议，含类型标识和资源定位，支持跨语言数据交换。模块3提供gRPC数据传输服务，支持单向和流式RPC，含元数据传输和状态检查功能。 |
| [config](config/_module.md) | package | Java Spring Boot配置类集合：DataSourceConfig配置数据源和JPA；ConfigProperties管理应用参数；AsyncTaskConfig定义异步任务执行器；CommonConfig处理通用设置。 |
| [listener](listener/_module.md) | package | InitListener监听应用启动事件，初始化存储服务，加载各类数据到缓存，启动gRPC服务和消息转发任务。失败时系统退出。 |
| [service](service/_module.md) | package | 分布式系统健康管理框架，含网关检测、微服务状态检查，支持本地预检和远程验证。提供数据传输元数据持久化、缓存管理和跨节点通信，含多种处理器和检查点机制，依赖多种基础设施。 |
| [common](common/_module.md) | package | ReturnStatusBuilder类提供构建返回状态的方法。GrpcServerScopeEnum定义gRPC服务范围枚举。GrpcConstant包含gRPC通信常量。EndpointBuilder处理网络端点创建转换。MessageEntityBuilder创建消息实体。ReturnStatusEnum定义返回状态枚举。TransferMetaCachePersistentTypeEnum表示持久化类型。RpcServerStatusEnum标识gRPC服务器状态。KeyValueDataBuilder构建键值数据。StorageConstant定义存储相关常量。 |
| [util](util/_module.md) | package | DatabaseEncryptConverter实现数据库字段加密解密。ClassUtil加载带特定注解的类。ReturnStatusUtil检查状态。TlsUtil处理证书。ExceptionUtil获取堆栈信息。SerializeUtil提供序列化功能。TransferMetaUtil提取消息信息。DatabaseEncryptUtil提供加密解密。GrpcUtil处理gRPC通信。 |
| [sdk](sdk/_module.md) | package | BoardHelper是处理HTTP请求的工具类，含POST和RESP_CODE_SUCCESS常量，提供push发送请求、generateReqParam生成参数、generateSign签名功能。UnionHelper处理联盟网络请求，含getMembers查询成员和getCaCertificate查询CA证书方法，均通过HTTP交互并验证响应。 |
| [repository](repository/_module.md) | package | 定义了多个Spring数据仓库接口，均继承基类提供CRUD功能。包括CertKeyInfo、FlowActionQueue、MessageQueue、CertRequestInfo、Message、CertInfo、Blacklist、GlobalConfig和PartnerConfig等实体操作仓库。GlobalConfigRepository额外提供findByGroup查询方法。 |
| [interceptor](interceptor/_module.md) | package | SystemTimestampMetadataBuilder构建带时间戳的元数据。AntiTamperServerInterceptor验证签名防篡改。SignVerifyServerInterceptor检查签名有效性。SignVerifyMetadataBuilder生成签名元数据。AbstractServerInterceptor提供拦截基础功能。AbstractCallCredentials处理凭证逻辑。ClientCallCredentials初始化客户端凭证。AbstractMetadataBuilder为元数据构建基类。SystemTimestampVerifyServerInterceptor验证时间戳。AntiTamperMetadataBuilder生成防篡改签名。IpAddressWhiteListServerInterceptor实现IP白名单控制。 |
| [init](init/_module.md) | package | 该模块管理gRPC服务器生命周期，支持双通道通信与动态TLS配置，包含启动/停止控制及拦截器管理。关键结构为GrpcServerContext和TLS证书上下文。依赖MemberService和ServerCertService。其他类负责缓存加载（黑名单、成员信息、传输元数据等）和存储初始化（持久化、函数计算）。 |


