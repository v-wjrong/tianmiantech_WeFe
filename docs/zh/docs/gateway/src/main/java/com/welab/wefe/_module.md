# 基础信息

|      |      |
|------|------|
| 名称 | wefe |
| 编码语言 | .java |
| 代码路径 | WeFe/gateway/src/main/java/com/welab/wefe |
| 包名 | docs.gateway.src.main.java.com.welab.wefe |
| 概述说明 | gRPC网关系统，含服务器管理、缓存加载、安全拦截、数据传输、存储访问、定时刷新、健康检查等功能模块，支持双通道通信、动态TLS、流式处理及分布式监控。 |

# 说明

## 概述  
该模块是分布式系统的核心通信网关，集成gRPC服务管理、安全拦截、数据流式传输与缓存同步四大功能，类似微服务架构的中枢神经系统。统一接口规范涵盖服务器控制（启动/停止/TLS切换）、安全元数据构建（签名/时间戳）、流式传输协议（GatewayMetaProto）及缓存操作API（refreshCache）。关键数据结构包括GrpcServerContext、TransferMeta传输元数据、StorageLocator存储定位器及各类Cache单例（如MemberBlacklistCache）。外部依赖涉及gRPC框架、Protobuf序列化、Spring Data JPA、TLS/SSL协议及云平台服务。例如通过AntiTamperServerInterceptor实现请求防篡改，PushDataSourceRequestStreamObserver处理双向流数据。

## 主要业务场景  
模块支撑三大典型场景：1)安全通信链（IP白名单→签名验证→TLS加密→防重放），类似API网关的零信任架构；2)流式数据管道（客户端推送→存储定位→状态反馈），采用生产者-消费者模型；3)缓存热加载体系（定时刷新→异常回滚→异步处理），如每10秒同步黑名单数据。业务流程整合端口校验、服务注册、证书管理及跨节点传输，交互模式涵盖链式拦截（类似Servlet过滤器）、构建器模式（StorageLocator动态配置）和注解驱动（@GrpcServer服务注册）。典型应用包括联盟成员管理（通过UnionHelper查询CA证书）、分片存储路由（使用fragment字段）及TLS热更新（restartExternalServer触发）。API类型覆盖一元RPC、流式接口及Spring Data仓库，集成案例丰富如DatabaseEncryptUtil实现SM4字段加密，InitListener完成gRPC服务冷启动。


### 包内部结构视图

```mermaid
graph TD
    wefe --> gateway
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

该流程图展示了WeFe网关项目的完整目录结构，从顶层wefe节点开始，逐级展开到各个子模块和文件。主要包含gateway主模块及其下的init、interceptor、api、service等15个核心子模块，每个子模块又进一步细分为具体功能组件和实现类。例如service模块下包含processors处理器和base基础服务，processors又分为available可用性检查和各类刷新处理器。整体结构清晰展现了项目的分层设计和功能划分，共包含约150个节点，完整覆盖了网关系统的配置、缓存、调度、实体、服务等所有关键组件。

# 文件列表

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| [gateway](gateway/_module.md) | package | gRPC网关系统，含服务器管理、缓存加载、安全拦截、数据传输、存储访问、定时刷新、健康检查等功能模块，支持双通道通信、动态TLS、流式处理及分布式监控。 |


