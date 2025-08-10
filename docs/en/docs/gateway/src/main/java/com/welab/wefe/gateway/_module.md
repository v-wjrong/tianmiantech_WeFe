# Basic Information

|      |      |
|------|------|
| Name | gateway |
| Language | .java |
| Code Path | WeFe/gateway/src/main/java/com/welab/wefe/gateway |
| Package Name | docs.gateway.src.main.java.com.welab.wefe.gateway |
| Brief Description | The gRPC gateway system includes functional modules such as server management, cache loading, security interception, data transmission, storage access, scheduled refreshing, and health checks. It supports dual-channel communication, dynamic TLS, streaming processing, and distributed monitoring. |

# Description

## Overview  
This module serves as the core communication gateway for distributed systems, integrating four key functionalities: gRPC service management, security interception, streaming data transmission, and cache synchronization. It operates akin to the central nervous system of a microservices architecture. The unified interface specification encompasses server control (start/stop/TLS switching), security metadata construction (signature/timestamp), streaming protocols (GatewayMetaProto), and cache operation APIs (refreshCache). Key data structures include GrpcServerContext, TransferMeta for transmission metadata, StorageLocator for storage positioning, and various Cache singletons (e.g., MemberBlacklistCache). External dependencies involve the gRPC framework, Protobuf serialization, Spring Data JPA, TLS/SSL protocols, and cloud platform services. For instance, request tamper-proofing is achieved via AntiTamperServerInterceptor, while bidirectional streaming data is handled by PushDataSourceRequestStreamObserver.  

## Core Business Scenarios  
The module supports three primary scenarios: 1) Secure communication chains (IP whitelisting → signature verification → TLS encryption → anti-replay), resembling a zero-trust architecture for API gateways; 2) Streaming data pipelines (client push → storage positioning → status feedback), adopting a producer-consumer model; 3) Cache hot-loading systems (scheduled refresh → exception rollback → asynchronous processing), such as synchronizing blacklist data every 10 seconds. Business processes integrate port validation, service registration, certificate management, and cross-node transmission, with interaction patterns including chain interception (similar to Servlet filters), builder patterns (dynamic configuration of StorageLocator), and annotation-driven approaches (@GrpcServer service registration). Typical applications include alliance member management (querying CA certificates via UnionHelper), sharded storage routing (using the fragment field), and TLS hot updates (triggered by restartExternalServer). API types span unary RPC, streaming interfaces, and Spring Data repositories, with integration examples like DatabaseEncryptUtil for SM4 field encryption and InitListener for cold-starting gRPC services.


### Package Internal Structure View

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

This flowchart presents the complete directory structure of the WeFe gateway project, starting from the top-level gateway node and expanding hierarchically to various submodules and files. The project comprises 14 main modules, with the service module being the most complex, containing two submodules (processors and base), where processors is further divided into available and checkpoint levels. The overall structure clearly demonstrates the functional partitioning of the gateway system, including initialization modules, interceptors, API services, data access layers, utility classes, and various service implementation classes.

# File List

| Name   | Type  | Description |
|-------|------|-------------|
| [base](base/_module.md) | package | The `Processor` annotation marks a class as a Spring component, containing type and description elements. `GrpcServerAnnotate` manages services annotated with `GrpcServer`, maintaining a global mapping that includes attributes such as service objects, scope, and interceptors. The `GrpcServer` annotation marks gRPC components, with configurations such as name, scope, and interceptors. `ProcessorAnnotate` manages processors annotated with `Processor`, maintaining a global mapping that includes name, description, and processor objects. |
| [cache](cache/_module.md) | package | RecvTransferMetaCache manages transfer metadata caching, GrpcChannelCache handles gRPC channels, PartnerConfigCache caches partner configurations, CaCertificateCache stores CA certificates, MemberCache manages member information, SystemConfigCache processes IP whitelists, CountDownLatchCache oversees latches, MemberBlacklistCache maintains blacklists, and SendTransferMetaCache manages transfer data queues. All are implemented as thread-safe singletons. |
| [scheduler](scheduler/_module.md) | package | Five Spring scheduled task classes, refreshing partner configurations, system configurations, member blacklists, members, and CA certificate caches every 10/30 seconds respectively, each with start/success/failure log records. |
| [entity](entity/_module.md) | package | CertInfoEntity stores certificate content, CSR ID, and status. PartnerConfigEntity records member ID and gateway address. MessageEntity manages message producers, levels, content, etc. MemberEntity contains member information, network configuration, and TLS status. MessageQueueEntity handles message queue data. BlacklistEntity stores blacklisted member IDs. CertKeyInfoEntity saves key PEM and algorithm. FlowActionQueueEntity manages action queues. FlagEntity is an empty class. AbstractBaseEntity defines creation/update information. CertRequestInfoEntity stores certificate request details. GlobalConfigEntity manages encryption configuration items. |
| [GatewayServer.java](GatewayServer.md) | file | SpringBoot gateway service main class, enabling component scanning, scheduled tasks, and asynchronous processing, excluding data source auto-configuration, and providing global application context access. |
| [api](api/_module.md) | package | Module 1 enables bidirectional streaming data transmission, processes TransferMeta data, and includes request/response stream interfaces, relying on asynchronous coordination mechanisms. Module 2 defines the Protobuf storage protocol, incorporating type identification and resource localization, and supports cross-language data exchange. Module 3 provides gRPC data transmission services, supporting both unary and streaming RPCs, along with metadata transmission and status check functionalities. |
| [config](config/_module.md) | package | Java Spring Boot Configuration Classes Collection: DataSourceConfig for configuring data sources and JPA; ConfigProperties for managing application parameters; AsyncTaskConfig for defining asynchronous task executors; CommonConfig for handling general settings. |
| [listener](listener/_module.md) | package | InitListener monitors application startup events, initializes storage services, loads various data into the cache, and starts gRPC services and message forwarding tasks. The system exits upon failure. |
| [service](service/_module.md) | package | Distributed System Health Management Framework, including gateway detection, microservice status checks, supporting local pre-checks and remote validation. Provides data transmission metadata persistence, cache management, and cross-node communication, featuring multiple processors and checkpoint mechanisms, dependent on various infrastructures. |
| [common](common/_module.md) | package | The `ReturnStatusBuilder` class provides methods for constructing return statuses. `GrpcServerScopeEnum` defines the gRPC service scope enumeration. `GrpcConstant` contains gRPC communication constants. `EndpointBuilder` handles network endpoint creation and conversion. `MessageEntityBuilder` creates message entities. `ReturnStatusEnum` defines the return status enumeration. `TransferMetaCachePersistentTypeEnum` represents the persistence type. `RpcServerStatusEnum` identifies the gRPC server status. `KeyValueDataBuilder` constructs key-value data. `StorageConstant` defines storage-related constants. |
| [util](util/_module.md) | package | DatabaseEncryptConverter implements encryption and decryption for database fields. ClassUtil loads classes with specific annotations. ReturnStatusUtil checks statuses. TlsUtil handles certificates. ExceptionUtil retrieves stack trace information. SerializeUtil provides serialization functionality. TransferMetaUtil extracts message information. DatabaseEncryptUtil offers encryption and decryption. GrpcUtil manages gRPC communication. |
| [sdk](sdk/_module.md) | package | BoardHelper is a utility class for handling HTTP requests, containing POST and RESP_CODE_SUCCESS constants, and providing functionalities such as push for sending requests, generateReqParam for generating parameters, and generateSign for signing. UnionHelper manages consortium network requests, including methods like getMembers for querying members and getCaCertificate for retrieving CA certificates, both interacting via HTTP and validating responses. |
| [repository](repository/_module.md) | package | Multiple Spring Data repository interfaces are defined, all inheriting from a base class to provide CRUD functionality. These include repositories for entity operations such as CertKeyInfo, FlowActionQueue, MessageQueue, CertRequestInfo, Message, CertInfo, Blacklist, GlobalConfig, and PartnerConfig. The GlobalConfigRepository additionally provides a findByGroup query method. |
| [interceptor](interceptor/_module.md) | package | SystemTimestampMetadataBuilder constructs metadata with timestamps. AntiTamperServerInterceptor verifies signatures to prevent tampering. SignVerifyServerInterceptor checks signature validity. SignVerifyMetadataBuilder generates signature metadata. AbstractServerInterceptor provides foundational interceptor functionality. AbstractCallCredentials handles credential logic. ClientCallCredentials initializes client credentials. AbstractMetadataBuilder serves as the base class for metadata construction. SystemTimestampVerifyServerInterceptor verifies timestamps. AntiTamperMetadataBuilder generates tamper-proof signatures. IpAddressWhiteListServerInterceptor implements IP whitelist control. |
| [init](init/_module.md) | package | This module manages the gRPC server lifecycle, supporting dual-channel communication and dynamic TLS configuration, including startup/shutdown control and interceptor management. The key structures are GrpcServerContext and TLS certificate context. It depends on MemberService and ServerCertService. Other classes are responsible for cache loading (blacklist, member information, transport metadata, etc.) and storage initialization (persistence, function computation). |


