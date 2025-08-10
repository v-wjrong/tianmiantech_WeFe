# Basic Information

|      |      |
|------|------|
| Name | union |
| Language | .java |
| Code Path | WeFe/union |
| Package Name | docs.union |
| Brief Description | The consortium chain management module provides member, data, contract, and monitoring management, adopting a layered interface design and relying on FISCO BCOS and Spring. The data synchronization module is responsible for on-chain event parsing and persistence, supporting multi-threaded ETL processes, and depends on MongoDB and node SDK. |

# Description

## Overview  
This module group is a comprehensive management system in a consortium blockchain environment, with core responsibilities including member lifecycle management, data resource operations, smart contract encapsulation, and blockchain data synchronization, akin to a combination of enterprise-level RBAC and blockchain ETL pipelines. The interface specification adopts a layered design, encompassing AbstractApi base class inheritance, @Api annotation definitions, standardized DTO encapsulation, and factory pattern parsers (e.g., MemberContractEventParser). Key data structures include member information (MemberQueryOutput), event objects (EventBO), smart contract return values (Tuple), and block metadata (BlockInfoBO). External dependencies involve the FISCO BCOS SDK, national cryptographic algorithm libraries, MongoDB, the Spring framework, and WeChat notification APIs. For instance, MemberService manages the member registration process, BlockSyncHeightService implements block height synchronization, and AbiUtil handles contract ABI parsing.

## Core Business Scenarios  
The module supports four major workflows: 1) Full member lifecycle management (registration → authentication → status updates), coordinated with smart contracts via MemberService; 2) Data resource CRUD and permission control, employing a dual-phase model of "local validation + on-chain operations"; 3) Blockchain data synchronization, resembling an ETL pipeline with the InitListener→DataSyncTask→Parser→persistence flow; 4) System monitoring and health checks. Interaction modes include RESTful APIs (e.g., member/realname/auth), static utility classes (FileCheckerUtil), and event-driven approaches (e.g., UnionNodeContractEventParser). Typical applications cover feature set queries, file synchronization, and certificate status transitions, with functional completeness reflected in fine-grained permissions, heterogeneous data conversion (MapperUtil), and thread-safe height update mechanisms.


### Package Internal Structure View

None

# File List

| Name   | Type  | Description |
|-------|------|-------------|
| [blockchain-data-sync](blockchain-data-sync/src/main/java/com/_module.md) | module | The core components of the blockchain data synchronization system include parsers, utility classes, service layer, and configuration management. Parsers convert contract events into MongoDB operations, utility classes provide auxiliary functions, the service layer handles data persistence, and configuration management initializes the environment. It supports multi-threaded synchronization to ensure data consistency. |
| [union-service](union-service/src/main/java/com/_module.md) | module | The Alliance Service Module Cluster provides multi-dimensional management capabilities, including member lifecycle, data resource operations, public services, and monitoring. It adopts RESTful interfaces, uniformly inheriting the AbstractApi base class, with key structures such as MemberOutput. It supports four major scenarios: member management, data CRUD, public services, and health checks. Relying on components like MemberService, it integrates smart contracts and blockchain technology to achieve federated learning data collaboration and permission control. |


