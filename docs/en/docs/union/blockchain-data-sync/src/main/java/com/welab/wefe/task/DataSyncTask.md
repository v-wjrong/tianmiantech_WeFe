# Basic Information

|      |      |
|------|------|
| Name | DataSyncTask |
| Language | .java |
| Code Path | WeFe/union/blockchain-data-sync/src/main/java/com/welab/wefe/task/DataSyncTask.java |
| Package Name | com.welab.wefe.task |
| Dependencies | ['com.welab.wefe.bo.data.BlockInfoBO', 'com.welab.wefe.bo.data.EventBO', 'com.welab.wefe.common.data.mongodb.entity.union.BlockSyncContractHeight', 'com.welab.wefe.common.data.mongodb.entity.union.BlockSyncHeight', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.util.ThreadUtil', 'com.welab.wefe.constant.BlockConstant', 'com.welab.wefe.constant.SyncConstant', 'com.welab.wefe.exception.BusinessException', 'com.welab.wefe.parser.BlockInfoParser', 'com.welab.wefe.service.BlockSyncContractHeightService', 'com.welab.wefe.service.BlockSyncDetailInfoService', 'com.welab.wefe.service.BlockSyncHeightService', 'com.welab.wefe.service.TransactionResponseService', 'com.welab.wefe.tool.DataProcessor', 'com.welab.wefe.tool.DataSyncContext', 'com.welab.wefe.util.BlockUtil', 'org.apache.commons.collections4.CollectionUtils', 'org.apache.commons.lang.math.NumberUtils', 'org.fisco.bcos.sdk.BcosSDK', 'org.fisco.bcos.sdk.client.Client', 'org.fisco.bcos.sdk.client.protocol.response.BcosBlock', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.beans.BeanUtils', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.beans.factory.annotation.Value', 'org.springframework.stereotype.Component', 'java.math.BigInteger', 'java.util.ArrayList', 'java.util.List'] |
| Brief Description | The DataSyncTask class is used for synchronizing blockchain data, including group ID configuration and WeChat notification URL. It synchronizes block data by group through multi-threading, handles exceptions, and records synchronization status. |

# Description

The DataSyncTask is a component class designed for data synchronization, which implements blockchain data synchronization functionality by injecting multiple services and configuration parameters. It primarily includes the startTask method to initiate synchronization tasks, checking the configured group ID and asynchronously executing the CrawlRunner. The CrawlRunner is an internal class responsible for continuously synchronizing block data for specified groups, including querying synchronized blocks, processing new blocks, and filtering synchronized contract events. During synchronization, it logs events, handles exceptions, and saves synchronization results and error information through related services. Overall, it achieves an efficient and stable blockchain data synchronization mechanism.

# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| DataSyncTask | class | The DataSyncTask class is a data synchronization task component that synchronizes blockchain data through multi-threading, incorporating error handling and filtering of already synchronized events. |



## Class DataSyncTask

|      |      |
|------|------|
| Access Modifier | @Component;public |
| Type | class |
| Name | DataSyncTask |
| Description | The DataSyncTask class is a data synchronization task component that synchronizes blockchain data through multi-threading, incorporating error handling and filtering of already synchronized events. |


### UML Class Diagram

```mermaid
classDiagram
    class DataSyncTask {
        -Logger LOG
        -BcosSDK bcosSDK
        -BlockSyncHeightService blockSyncHeightService
        -BlockSyncContractHeightService blockSyncContractHeightService
        -BlockSyncDetailInfoService blockSyncDetailInfoService
        -TransactionResponseService transactionResponseService
        -String dataSyncGroupId
        -String wechatUrl
        +startTask()
        +CrawlRunner~inner~
    }

    class CrawlRunner {
        -int groupId
        -Client client
        +CrawlRunner(int groupId)
        +run()
        -startSync(long blockNumber) void
        -filterBlockInfoBO(BlockInfoBO blockInfoBO) BlockInfoBO
    }

    class BcosSDK {
        <<Interface>>
        +getClient(int groupId) Client
    }

    class BlockSyncHeightService {
        <<Interface>>
        +findByGroupId(String groupId) BlockSyncHeight
        +sendErrorMsg(int groupId, long blockNumber, Exception e) void
        +save(BlockInfoBO blockInfoBO) void
    }

    class BlockSyncContractHeightService {
        <<Interface>>
        +findByGroupIdAndContractName(String groupId, String contractName) BlockSyncContractHeight
        +save(BlockInfoBO blockInfoBO) void
    }

    class BlockSyncDetailInfoService {
        <<Interface>>
        +saveBlockDetailInfo(BlockInfoBO blockInfoBO) void
    }

    class TransactionResponseService {
        <<Interface>>
        +save(BlockInfoBO blockInfoBO) void
    }

    DataSyncTask --> BcosSDK : Dependency
    DataSyncTask --> BlockSyncHeightService : Dependency
    DataSyncTask --> BlockSyncContractHeightService : Dependency
    DataSyncTask --> BlockSyncDetailInfoService : Dependency
    DataSyncTask --> TransactionResponseService : Dependency
    DataSyncTask *-- CrawlRunner : Composition
    CrawlRunner --> BcosSDK : Invoke
    CrawlRunner --> BlockSyncHeightService : Invoke
    CrawlRunner --> BlockSyncContractHeightService : Invoke
    CrawlRunner --> BlockSyncDetailInfoService : Invoke
    CrawlRunner --> TransactionResponseService : Invoke
```

This code demonstrates the implementation of a blockchain data synchronization task, primarily consisting of the main DataSyncTask class and its inner class CrawlRunner. DataSyncTask obtains multiple service interface instances through dependency injection, including the BcosSDK client and various block synchronization services. CrawlRunner implements the Runnable interface and is responsible for the concrete block synchronization logic, encompassing block data retrieval, filtering, processing, and persistence. The overall design adopts a layered architecture, where the main task class handles scheduling while the inner class manages specific business logic, achieving module decoupling through service interfaces. The synchronization process incorporates error handling, retry mechanisms, and progress tracking to ensure the reliability and integrity of data synchronization.


### Internal Method Call Graph

```mermaid
graph TD
    A["Class DataSyncTask"]
    B["Attribute: Logger LOG"]
    C["Attribute: BcosSDK bcosSDK"]
    D["Attribute: BlockSyncHeightService blockSyncHeightService"]
    E["Attribute: BlockSyncContractHeightService blockSyncContractHeightService"]
    F["Attribute: BlockSyncDetailInfoService blockSyncDetailInfoService"]
    G["Attribute: TransactionResponseService transactionResponseService"]
    H["Attribute: String dataSyncGroupId"]
    I["Attribute: String wechatUrl"]
    J["Method: startTask()"]
    K["Inner Class: CrawlRunner"]
    L["Method: run()"]
    M["Method: startSync(long blockNumber)"]
    N["Method: filterBlockInfoBO(BlockInfoBO blockInfoBO)"]

    A --> B
    A --> C
    A --> D
    A --> E
    A --> F
    A --> G
    A --> H
    A --> I
    A --> J
    A --> K
    K --> L
    K --> M
    K --> N

    J --> J1["Check if dataSyncGroupId is empty"]
    J1 -->|Yes| J2["Log warning and return"]
    J1 -->|No| J3["Split groupIds and iterate"]
    J3 --> J4["Check if numeric"]
    J4 -->|Yes| J5["Create CrawlRunner async thread"]
    J4 -->|No| J6["Skip current group"]

    L --> L1["Get client and create dataSyncContext"]
    L1 --> L2["Query synced block height"]
    L2 --> L3["Get current max block height"]
    L3 --> L4["Check if new block waiting needed"]
    L4 -->|Yes| L5["Sleep 500ms then continue"]
    L4 -->|No| L6["Iterate pending blocks"]
    L6 --> L7["Call startSync to sync block"]
    L7 -->|Success| L8["Increment block number"]
    L7 -->|Business exception| L9["Send error message and terminate"]
    L7 -->|Other exception| L10["Send error message and retry"]

    M --> M1["Retry 10 times to get block data"]
    M1 --> M2["Parse block info"]
    M2 --> M3["Filter synced contract events"]
    M3 --> M4["Process block data"]
    M4 --> M5["Save contract height"]
    M5 --> M6["Save block details"]
    M6 --> M7["Save block height"]
    M7 --> M8["Save transaction response"]

    N --> N1["Copy BlockInfoBO"]
    N1 --> N2["Filter synced events"]
    N2 --> N3["Return filtered object"]
```

This code implements a blockchain data synchronization task, primarily consisting of the DataSyncTask class and its inner class CrawlRunner. The flowchart illustrates the complete workflow from task initiation to block synchronization: first validating configuration parameters, then creating asynchronous threads for each group; during synchronization, it checks block height differences, retrieves block data through retry mechanisms, filters processed events, and saves various types of information. The entire process incorporates robust exception handling and logging mechanisms, achieving incremental blockchain data synchronization through multi-service collaboration.

### Field List

| Name  | Type  | Description |
|-------|-------|------|
| blockSyncContractHeightService | BlockSyncContractHeightService | Automatically inject the block synchronization contract height service instance. |
| LOG = LoggerFactory.getLogger(DataSyncTask.class) | Logger | Define a private static log object LOG for the DataSyncTask class. |
| transactionResponseService | TransactionResponseService | The code snippet uses the @Autowired annotation to automatically inject an instance of TransactionResponseService. |
| blockSyncHeightService | BlockSyncHeightService | Automatically injects the block synchronization height service instance. |
| blockSyncDetailInfoService | BlockSyncDetailInfoService | The code snippet uses the @Autowired annotation to automatically inject an instance of the BlockSyncDetailInfoService. |
| dataSyncGroupId | String | The code snippet defines a private String variable dataSyncGroupId, whose value is injected from the configuration item contract.data-sync-group-id via the @Value annotation. |
| wechatUrl | String | WeChat bot URL configuration item, injected into the private variable `wechatUrl` via @Value. |
| bcosSDK | BcosSDK | Use @Autowired to automatically inject a BcosSDK instance. |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| startTask | void | Method checks the configuration of the data synchronization group IDs. If it is empty, a warning is issued and the process returns. Otherwise, it splits the group IDs into an array, iterates over each ID, skips non-numeric items, and initiates an asynchronous crawling task for each valid ID. |




