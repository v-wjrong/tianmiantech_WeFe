# Basic Information

|      |      |
|------|------|
| Name | manager |
| Language | .java |
| Code Path | WeFe/manager |
| Package Name | docs.manager |
| Brief Description | The digital certificate management module implements the entire process of application, issuance, and key binding. The core component CertOperationService relies on CertDao for persistence, with data structures including CertRequestVO, etc., using FastJSON for serialization, and exceptions handled by CertMgrException. The consortium chain management system is responsible for multi-dimensional resource management and smart contract interaction, adopting a layered design that supports scenarios such as member registration and data tagging. It depends on MongoDB, FISCO BCOS SDK, etc., with functionalities covering state management and permission verification. |

# Description

## Overview  
This module implements full lifecycle management of multi-dimensional resources in a consortium blockchain ecosystem. Its core responsibilities include digital certificate management (application/issuance/key binding), member collaboration, and smart contract interaction, functioning similarly to an enterprise-grade RBAC combined with a distributed configuration center. The interface specification follows a layered design: the RESTful API layer inherits from the AbstractApi base class, the contract layer provides CRUD/event subscription, and the configuration layer supports dynamic loading. Key data structures include CertRequestVO (certificate application), CertVO (certificate entity), InsertEventResponse (on-chain response), and version number strings. External dependencies, after deduplication, consist of Java base libraries, BouncyCastle, FastJSON, MongoDB driver, FISCO BCOS SDK, and national cryptographic algorithm libraries. For example, CertOperationService synchronizes on-chain and off-chain states, while TransformUtils copies properties via reflection.

## Core Business Scenarios  
The workflow forms two closed loops: a collaboration loop ("member registration → resource upload → permission configuration") and a certificate management loop ("application → issuance → binding"), resembling a hybrid of a ticketing system and an event bus. Interaction modes include chained parameter validation at the API layer (e.g., UnionNode series APIs for node maintenance) and event-driven operations at the contract layer (e.g., file uploads triggering insertEvent). Typical applications involve administrators maintaining node lists and users generating data tag clouds. Functional completeness is reflected in each entity's state management and off-chain monitoring capabilities (e.g., MemberContract managing public keys). API types encompass queries (QueryAllApi), operations (DeleteByTagId), and file-related actions (DownloadApi), forming a three-stage processing flow: configuration → business → blockchain.


### Package Internal Structure View

None

# File List

| Name   | Type  | Description |
|-------|------|-------------|
| [manager-service](manager-service/src/main/java/com/_module.md) | module | The digital certificate management module implements the entire process of application, issuance, and key binding. The core component CertOperationService relies on CertDao for persistence, with data structures including CertRequestVO, etc., using FastJSON for serialization, and exceptions handled by CertMgrException. The consortium chain management system is responsible for multi-dimensional resource management and smart contract interaction, adopting a layered design that supports scenarios such as member registration and data tagging. It relies on MongoDB, FISCO BCOS SDK, etc., with functionalities covering state management and permission verification. |


