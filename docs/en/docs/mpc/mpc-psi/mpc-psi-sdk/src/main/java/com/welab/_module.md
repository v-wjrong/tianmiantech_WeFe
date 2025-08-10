# Basic Information

|      |      |
|------|------|
| Name | welab |
| Language | .java |
| Code Path | WeFe/mpc/mpc-psi/mpc-psi-sdk/src/main/java/com/welab |
| Package Name | docs.mpc.mpc-psi.mpc-psi-sdk.src.main.java.com.welab |
| Brief Description | This SDK implements multi-party Private Set Intersection (PSI) functionality, supporting ECDH and DH encryption protocols. It includes server/client components, data preprocessing tools, and a factory pattern. The core workflow consists of key generation, data encryption, and result comparison, with performance optimized through multithreading, making it suitable for secure data matching scenarios. |

# Description

## Overview  
This module is a Privacy-Preserving Set Intersection (PSI) toolkit within Secure Multi-Party Computation (MPC), with core responsibilities including private data matching based on Elliptic Curve Cryptography (ECDH) and Diffie-Hellman (DH) protocols, data preprocessing, and result querying. The module adopts a layered design: the底层 provides foundational cryptographic capabilities (e.g., point multiplication for ECDH-PSI), the中层 implements data partitioning/format conversion (e.g., PartitionUtil for sharding), and the上层 encapsulates service interfaces (e.g., PrivateSetIntersectionService). Key data structures encompass elliptic curve parameters, encrypted mapping tables, partitioned sets, and obfuscated data models, with dependencies limited to the Java standard library and cryptographic algorithm libraries. For instance, EcdhPsi employs hashToCurve for data encryption, while PsiFactory uses the factory pattern to create protocol instances.

## Key Business Scenarios  
The module supports three typical scenarios: 1) Secure user matching (ECDH-PSI bidirectional encrypted intersection); 2) Batch data preprocessing (sharding → conversion → encryption pipeline); 3) Private information retrieval (Naor-Pinkas oblivious transfer). The complete workflow follows the "key generation → data encryption → result intersection" model, akin to multi-party key negotiation. For example, DhPsiServer uses concurrent hash tables to accelerate ciphertext comparison, while PirQuery achieves anonymous queries via Diffie-Hellman exchange. Interaction modes include client-server architecture (e.g., EcdhPsiClient) and factory pattern (PsiFactory), with APIs covering key operations, dataset encryption, and paginated result merging, making it suitable for cross-institutional secure data computation scenarios.


### Package Internal Structure View

```mermaid
graph TD
    wefe --> mpc
    mpc --> psi
    psi --> sdk
    sdk --> ecdh
    sdk --> util
    sdk --> service
    sdk --> excel
    sdk --> pir
    sdk --> dh
    sdk --> model
    sdk --> Psi.java
    sdk --> EcdhPsi.java
    sdk --> PsiFactory.java
    sdk --> PrivateSetIntersection.java
    ecdh --> EllipticCurve.java
    ecdh --> EcdhPsiServer.java
    ecdh --> EcdhPsiClient.java
    util --> PartitionUtil.java
    util --> EcdhUtil.java
    util --> ConverterUtil.java
    service --> PrivateSetIntersectionService.java
    excel --> AbstractDataSetReader.java
    excel --> CsvDataSetReader.java
    excel --> ExcelDataSetReader.java
    excel --> ExcelReader.java
    pir --> PirQuery.java
    dh --> DhPsiServer.java
    dh --> DhPsiClient.java
    model --> ConfuseData.java
```

This flowchart illustrates the complete directory structure of the MPC-PSI-SDK module in the WeFe project, starting from the root directory `wefe` and hierarchically expanding to `mpc`, `psi`, and `sdk` directories. The `sdk` directory contains multiple submodules such as `ecdh`, `util`, `service`, etc., each of which includes specific implementation class files. The entire structure clearly presents the component distribution of the PSI (Private Set Intersection) SDK, including core classes, utility classes, service interfaces, and implementations of different protocols (ECDH/DH).

# File List

| Name   | Type  | Description |
|-------|------|-------------|
| [wefe](wefe/_module.md) | package | This SDK implements multi-party Private Set Intersection (PSI) functionality, supporting ECDH and DH encryption protocols. It includes server/client components, data preprocessing tools, and a factory pattern. The core workflow involves key generation, data encryption, and result comparison, with performance optimized through multithreading, making it suitable for secure data matching scenarios. |


