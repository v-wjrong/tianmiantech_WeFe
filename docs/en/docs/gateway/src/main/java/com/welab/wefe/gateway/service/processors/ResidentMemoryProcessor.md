# Basic Information

|      |      |
|------|------|
| Name | ResidentMemoryProcessor |
| Language | .java |
| Code Path | WeFe/gateway/src/main/java/com/welab/wefe/gateway/service/processors/ResidentMemoryProcessor.java |
| Package Name | com.welab.wefe.gateway.service.processors |
| Dependencies | ['com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.wefe.enums.GatewayProcessorType', 'com.welab.wefe.gateway.GatewayServer', 'com.welab.wefe.gateway.api.meta.basic.BasicMetaProto', 'com.welab.wefe.gateway.api.meta.basic.GatewayMetaProto', 'com.welab.wefe.gateway.base.Processor', 'com.welab.wefe.gateway.cache.RecvTransferMetaCache', 'com.welab.wefe.gateway.cache.RecvTransferMetaCountDownLatchCache', 'com.welab.wefe.gateway.common.ReturnStatusBuilder', 'com.welab.wefe.gateway.service.base.AbstractRecvTransferMetaCachePersistentService'] |
| Brief Description | Resident memory processor, processes transmission metadata, sets the status to completed and persists it. If successful, stores it in the cache (excluding content); if failed, marks it as erroneous and notifies the client. |

# Description

The ResidentMemoryProcessor is a memory-resident processor that inherits from AbstractProcessor. It handles remote transmission metadata by first setting the state to COMPLETE, then saving the data through the persistence service. If the save fails, it returns an error state; if successful, it clears the content and stores it in the cache. Any exceptions during processing are logged with the ERROR state set. Finally, it notifies the client of data arrival via the notifyClient method. The entire process ensures data persistence and state updates while preventing excessive cache growth.

# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| ResidentMemoryProcessor | class | Resident memory processor, processes transmission metadata, sets the status to completed and persists it, logs errors and notifies the client in case of exceptions, and notifies the client of data arrival upon success. |



## Class ResidentMemoryProcessor

|      |      |
|------|------|
| Access Modifier | @Processor(type = GatewayProcessorType.residentMemoryProcessor, desc = "Memory resident processor");public |
| Type | class |
| Name | ResidentMemoryProcessor |
| Description | Resident memory processor, processes transmission metadata, sets the status to completed and persists it, logs errors and notifies the client in case of exceptions, and notifies the client of data arrival upon success. |


### UML Class Diagram

```mermaid
classDiagram
    class ResidentMemoryProcessor {
        <<Processor>> 
        +remoteProcess(GatewayMetaProto~TransferMeta~ transferMeta) BasicMetaProto~ReturnStatus~
        -notifyClient(GatewayMetaProto~TransferMeta~ transferMeta) void
    }

    class AbstractProcessor {
        <<Abstract>>
    }

    class GatewayMetaProto~TransferMeta~ {
        +toBuilder() Builder
        +getTransferStatus() TransferStatus
        +getSessionId() String
        +getContent() Content
    }

    class RecvTransferMetaCache {
        +getInstance() RecvTransferMetaCache
        +put(String sessionId, GatewayMetaProto~TransferMeta~ meta) void
    }

    class AbstractRecvTransferMetaCachePersistentService {
        <<Abstract>>
        +save(GatewayMetaProto~TransferMeta~ meta) StatusCodeWithException
    }

    class StatusCodeWithException {
        +getStatusCode() StatusCode
        +getMessage() String
    }

    class RecvTransferMetaCountDownLatchCache {
        +getInstance() RecvTransferMetaCountDownLatchCache
        +openCountDownLatch(String sessionId) void
    }

    ResidentMemoryProcessor --|> AbstractProcessor : Inheritance
    ResidentMemoryProcessor --> GatewayMetaProto~TransferMeta~ : Processes
    ResidentMemoryProcessor --> RecvTransferMetaCache : Uses
    ResidentMemoryProcessor --> AbstractRecvTransferMetaCachePersistentService : Depends on
    ResidentMemoryProcessor --> RecvTransferMetaCountDownLatchCache : Notifies
    AbstractRecvTransferMetaCachePersistentService --> StatusCodeWithException : Returns
```

This diagram illustrates the ResidentMemoryProcessor class and its related dependencies. ResidentMemoryProcessor inherits from AbstractProcessor, processes GatewayMetaProto.TransferMeta objects, utilizes RecvTransferMetaCache for caching operations, depends on AbstractRecvTransferMetaCachePersistentService for persistence, and notifies clients via RecvTransferMetaCountDownLatchCache. The persistence service returns StatusCodeWithException status objects. The overall structure clearly demonstrates the interaction relationships between the processor and caching, persistence services, and client notification mechanisms.


### Internal Method Call Graph

```mermaid
graph TD
    A["ResidentMemoryProcessor.remoteProcess"]
    B["Set status to COMPLETE"]
    C["Get persistent service instance"]
    D["Call save method to persist data"]
    E["Check if status code is SUCCESS"]
    F["Cache cleaned transferMeta"]
    G["Catch exception and set ERROR status"]
    H["Cache error transferMeta after cleanup"]
    I["Call notifyClient to notify client"]
    J["Return success status"]
    K["Return error status"]

    A --> B
    B --> C
    C --> D
    D --> E
    E -- Yes --> F
    E -- No --> K
    F --> I
    A -- Exception --> G
    G --> H
    H --> I
    I --> K
    I --> J
```

```mermaid
sequenceDiagram
    participant Client
    participant ResidentMemoryProcessor
    participant RecvTransferMetaCache
    participant PersistentService
    participant CountDownLatchCache

    Client->>ResidentMemoryProcessor: remoteProcess(transferMeta)
    ResidentMemoryProcessor->>ResidentMemoryProcessor: setStatus(COMPLETE)
    ResidentMemoryProcessor->>GatewayServer: getBean(PersistentService)
    ResidentMemoryProcessor->>PersistentService: save(transferMeta)
    alt Save successful
        PersistentService-->>ResidentMemoryProcessor: SUCCESS
        ResidentMemoryProcessor->>RecvTransferMetaCache: put(cleanedMeta)
    else Save failed
        PersistentService-->>ResidentMemoryProcessor: FAILURE
        ResidentMemoryProcessor-->>Client: return error
    end
    ResidentMemoryProcessor->>CountDownLatchCache: openCountDownLatch
    CountDownLatchCache-->>Client: Notification received
    ResidentMemoryProcessor-->>Client: return success
```

This code demonstrates the core workflow of a resident memory processor, primarily handling the persistence of transfer metadata and client notification. The flowchart clearly illustrates both normal and exception handling paths, including key steps such as status setting, service acquisition, data persistence, cache operations, and client notification. The sequence diagram details the interaction sequence between components, particularly the collaboration between the persistent service and countdown latch cache. The entire design emphasizes exception handling and resource cleanup to ensure system stability.

### Field List

| Name  | Type  | Description |
|-------|-------|------|

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| remoteProcess | BasicMetaProto.ReturnStatus | This method processes transmission metadata, sets the status to completed, and persists the storage. If it fails, it logs the error and sets the status to error. Regardless of success or failure, it clears the content, caches the metadata, and notifies the client. It returns OK upon success or exception information upon failure. |
| notifyClient | void | This method is used to notify the client to open the countdown latch of the specified session ID by invoking the cache instance. |




