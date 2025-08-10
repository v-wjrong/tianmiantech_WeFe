# Basic Information

|      |      |
|------|------|
| Name | welab |
| Language | .java |
| Code Path | WeFe/fusion/fusion-core/src/main/java/com/welab |
| Package Name | docs.fusion.fusion-core.src.main.java.com.welab |
| Brief Description | The module implements the Private Set Intersection (PSI) protocol, including Server/Client base classes, data conversion, and metadata processing, relying on the RSA-PSI algorithm and JObject serialization. The Bloom filter module supports efficient operations and persistence, integrating cryptographic tools and thread pool management. The enumeration module defines key federated learning dimensions such as task status and algorithm types. The DTO module encapsulates Bloom filters and metadata, supporting serialized transmission of PSI protocol components. |

# Description

## Overview  
This module implements the dual-end logic of the Privacy-Preserving Set Intersection (PSI) protocol and federated learning support components. Its core responsibilities include secure data alignment (similar to blind signature processes), Bloom filter operations, and task status management. The interface specifications cover Server/Client abstract base classes, enumeration definitions, and DTO transmission models, such as `dataTransform` for data conversion and `generateBlindingFactor` for metadata download. Key data structures include `BigInteger` encryption parameters, `BitSet` bit collections, `BloomFilterDto` transmission objects, and enumerations like `PSIActuatorRole`. External dependencies involve the `JObject` serialization framework, RSA-PSI algorithms, and Java cryptography components. For example, `ActuatorCache` manages actuator mappings, while `BloomFilterUtils` simplifies I/O operations.  

## Key Business Scenarios  
The typical workflow follows Client initialization → metadata exchange → bucket encryption → Server matching → result return, adopting a multi-threaded paging approach similar to MapReduce. Complete functionalities cover data preprocessing (e.g., `parseAndMatch`), cryptographic transformations (RSA/DH algorithms), status coordination (`FusionTaskStatus` enumeration), and filter persistence (`writeTo`/`readFrom`). The interaction model is role-based (server/client) and state-driven (e.g., `Progress.Ready` triggers execution). API types include basic operations (`add`/`contains`), cryptographic functions (`generateKeys`), and thread pool task submissions. For instance, MD5 hashing ensures data consistency, `AlgorithmType.DH` supports key exchange, and the DTO pattern enables cross-node transmission.


### Package Internal Structure View

```mermaid
graph TD
    wefe --> fusion
    fusion --> core
    core --> actuator
    core --> utils
    core --> enums
    core --> dto
    actuator --> psi
    actuator --> ActuatorCache.java
    actuator --> AbstractActuator.java
    psi --> AbstractPsiServerActuator.java
    psi --> PsiClientInterface.java
    psi --> AbstractPsiActuator.java
    psi --> AbstractPsiClientActuator.java
    psi --> PsiServerInterface.java
    utils --> bf
    utils --> CryptoUtils.java
    utils --> PSIUtils.java
    utils --> FusionThreadPool.java
    bf --> BloomFilterUtils.java
    bf --> BloomFilters.java
    enums --> Options.java
    enums --> DBType.java
    enums --> ActionType.java
    enums --> PSIActuatorRole.java
    enums --> CallbackType.java
    enums --> Progress.java
    enums --> FusionTaskStatus.java
    enums --> DataResourceSource.java
    enums --> AlgorithmType.java
    enums --> PSIActuatorStatus.java
    dto --> BloomFilterDto.java
    dto --> PsiActuatorMeta.java
```

This flowchart illustrates the Java code structure of the fusion-core module in the WeFe project. Starting from the top-level package 'wefe', it hierarchically expands to the core component 'core', which is further subdivided into submodules such as actuators, utility classes (utils), enumerations (enums), and data objects (dto). The actuator module contains PSI-related implementation classes, the utils module includes tools like Bloom filters and cryptographic utilities, the enums define various system state types, and the dto module contains DTO classes for data transfer.

# File List

| Name   | Type  | Description |
|-------|------|-------------|
| [wefe](wefe/_module.md) | package | The module implements the Private Set Intersection (PSI) protocol, including Server/Client base classes, data conversion, and metadata processing, relying on the RSA-PSI algorithm and JObject serialization. The Bloom filter module supports efficient operations and persistence, integrating cryptographic tools and thread pool management. The enumeration module defines key federated learning dimensions such as task status and algorithm types. The DTO module encapsulates Bloom filters and metadata, supporting serialized transmission of PSI protocol components. |


