# Basic Information

|      |      |
|------|------|
| Name | welab |
| Language | .java |
| Code Path | WeFe/gateway/src/main/java/com/welab |
| Package Name | docs.gateway.src.main.java.com.welab |
| Brief Description | A gRPC gateway system comprising functional modules such as server management, cache loading, security interception, data transmission, storage access, scheduled refresh, and health checks, supporting dual-channel communication, dynamic TLS, stream processing, and distributed monitoring. |

# Description

## Overview  
This module serves as the core communication gateway for distributed systems, integrating four key functionalities: gRPC service management, security interception, streaming data transmission, and cache synchronization. It operates like the central nervous system of a microservices architecture. The unified interface specification encompasses server control (start/stop/TLS switching), security metadata construction (signature/timestamp), streaming protocols (GatewayMetaProto), and cache operation APIs (refreshCache). Key data structures include GrpcServerContext, TransferMeta for transmission metadata, StorageLocator for storage positioning, and various Cache singletons (e.g., MemberBlacklistCache). External dependencies involve the gRPC framework, Protobuf serialization, Spring Data JPA, TLS/SSL protocols, and cloud platform services. For example, AntiTamperServerInterceptor ensures request tamper-proofing, while PushDataSourceRequestStreamObserver handles bidirectional streaming data.  

## Core Business Scenarios  
The module supports three primary scenarios: 1) Secure communication chains (IP whitelisting → signature verification → TLS encryption → anti-replay), resembling a zero-trust architecture for API gateways; 2) Streaming data pipelines (client push → storage positioning → status feedback), adopting a producer-consumer model; 3) Cache hot-loading systems (scheduled refresh → exception rollback → asynchronous processing), such as synchronizing blacklist data every 10 seconds. Business processes integrate port validation, service registration, certificate management, and cross-node transmission, with interaction modes including chain interception (similar to Servlet filters), builder patterns (StorageLocator dynamic configuration), and annotation-driven approaches (@GrpcServer service registration). Typical applications include consortium member management (querying CA certificates via UnionHelper), sharded storage routing (using the fragment field), and TLS hot updates (triggered by restartExternalServer). API types range from unary RPCs and streaming interfaces to Spring Data repositories, with integration examples like DatabaseEncryptUtil for SM4 field encryption and InitListener for gRPC service cold starts.


### Package Internal Structure View

```mermaid
graph TD
    wefe --> gateway
    gateway --> init
    gateway --> interceptor
    gateway --> api
    gateway --> service
    gateway --> repository
    gateway --> sdk
    gateway --> util
    gateway --> common
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

This flowchart illustrates the complete directory structure of the WeFe gateway project, starting from the top-level wefe node and hierarchically expanding to gateway and all its submodules. The diagram clearly presents 12 main modules (such as init, interceptor, service, etc.) and their subordinate files, particularly highlighting the complex structure of the processors and base submodules under the service module. All nodes use end-path names, strictly adhering to the hierarchical relationships, and comprehensively covering all given path information.

# File List

| Name   | Type  | Description |
|-------|------|-------------|
| [wefe](wefe/_module.md) | package | The gRPC gateway system includes functional modules such as server management, cache loading, security interception, data transmission, storage access, scheduled refresh, and health checks. It supports dual-channel communication, dynamic TLS, streaming processing, and distributed monitoring. |


