# Basic Information

|      |      |
|------|------|
| Name | blockchain-data-sync |
| Language | .java |
| Code Path | WeFe/union/blockchain-data-sync |
| Package Name | docs.union.blockchain-data-sync |
| Brief Description | The core components of the blockchain data synchronization system include parsers, utility classes, service layer, and configuration management. Parsers convert contract events into MongoDB operations, utility classes provide auxiliary functions, the service layer handles data persistence, and configuration management initializes the environment. It supports multi-threaded synchronization to ensure data consistency. |

# Description

## Overview  
This module serves as the core component of the blockchain data synchronization system, featuring a layered architecture design. It is responsible for parsing, transforming, and persisting on-chain contract events. Key responsibilities include: event parsing via the abstract factory pattern (e.g., `MemberContractEventParser`), thread-safe data synchronization management (e.g., `SyncConstant`), and toolkit support (e.g., `AbiUtil`). Critical data structures encompass business objects like `EventBO`, block information such as `BlockInfoBO`, and metadata like `ContractABIDefinition`. External dependencies include MongoDB, blockchain node SDKs (e.g., `BcosBlock`), Java standard libraries, and WeChat notification APIs. For instance, `BlockSyncHeightService` enables idempotent block height updates, while `ClassPathScanHandler` dynamically loads parser classes.  

## Key Business Scenarios  
The module supports full lifecycle management of blockchain data in multi-threaded environments, resembling a hybrid of ETL pipelines and event bus patterns. A typical workflow involves: `InitListener` initializing the environment → `DataSyncTask` synchronizing blocks → `DataProcessor` routing events → subclass `Parser` handling business logic → MongoDB persistence. It primarily addresses three scenarios: entity state changes (e.g., member public key updates), metadata maintenance (e.g., ABI parsing), and resource permission management (e.g., dataset label control). Interaction modes are uniformly driven by static methods like `parseContractEvent`, such as `UnionNodeContractEventParser` handling node state changes and `BloomFilterContractEventParser` maintaining Bloom filter parameters. API types include factory methods, scanning interfaces, and data processing, with integration cases demonstrating thread-safe height updates and automatic contract parser discovery.


### Package Internal Structure View

None

# File List

| Name   | Type  | Description |
|-------|------|-------------|
| [com](src/main/java/com/_module.md) | folder | The core components of the blockchain data synchronization system include parsers, utility classes, service layer, and configuration management. Parsers convert contract events into MongoDB operations, utility classes provide auxiliary functions, the service layer handles data persistence, and configuration management initializes the environment. It supports multi-threaded synchronization to ensure data consistency. |


