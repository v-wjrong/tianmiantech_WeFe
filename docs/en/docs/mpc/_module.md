# Basic Information

|      |      |
|------|------|
| Name | mpc |
| Language | .java |
| Code Path | WeFe/mpc |
| Package Name | docs.mpc |
| Brief Description | This series of modules implements core functionalities of Secure Multi-party Computation (MPC): PIR (Private Information Retrieval), PSI (Private Set Intersection), key exchange, and secure aggregation. Utilizing protocols such as Naor-Pinkas, Hauck, and ECDH, it supports federated learning and joint risk control scenarios. The modules incorporate mechanisms like encrypted transmission, data obfuscation, and thread-safe caching, offering full lifecycle management through layered APIs and POJO specifications. |

# Description

## Overview  
This module serves as the core component of Secure Multi-party Computation (MPC), integrating functionalities such as Private Information Retrieval (PIR), Private Set Intersection (PSI), and Secure Aggregation (SA). It employs cryptographic techniques like the Naor-Pinkas/Hauck protocol, ECDH, and Diffie-Hellman to ensure data privacy protection. The unified interface specification encompasses six categories of operations: PIR basic interfaces (e.g., generate/query), PSI service interfaces (e.g., PrivateSetIntersectionService), key exchange (e.g., queryDiffieHellmanKey), and result aggregation (e.g., QuerySAResult). Key data structures are aggregated into Diffie-Hellman parameters (p/g), encrypted mapping tables, session identifiers (UUID), and obfuscated data models, relying on cryptographic libraries such as BouncyCastle/JCE, thread pools, and JSON utilities. For instance, bidirectional encrypted set intersection is achieved via EcdhPsi, while SecureAggregation leverages random seeds to implement differential privacy.

## Key Business Scenarios  
The module supports federated learning and joint risk control scenarios, with a typical workflow involving hierarchical secure computation: 1) Diffie-Hellman key exchange (similar to TLS handshake); 2) PSI data matching (bidirectional encrypted set intersection via ECDH); 3) PIR privacy retrieval (Naor-Pinkas protocol) and result aggregation. The interaction model adopts a dual-track API system, where synchronous interfaces handle immediate requests (e.g., getHauckTarget), and asynchronous services manage background tasks (e.g., HuackKeyService thread pool). Functional completeness spans the entire lifecycle from key management and data obfuscation to secure transmission. For example, DhPsiServer accelerates ciphertext comparison, while QueryResultService supports weight configuration. The API features a layered design, with foundational layers like static methods in DiffieHellmanUtil and protocol layers such as object-oriented operations in QuerySAResultRequest, making it suitable for cross-institution secure computation.


### Package Internal Structure View

None

# File List

| Name   | Type  | Description |
|-------|------|-------------|
| [mpc-sa](mpc-sa/mpc-sa-sdk/src/main/java/com/_module.md) | module | This module implements query processing and key exchange functionalities in secure multi-party computation, supporting differential privacy and cache management. It includes fixed/custom factor queries and DH key generation interfaces, relies on a caching system, and is suitable for scenarios such as federated learning. |
| [mpc-psi](mpc-psi/mpc-psi-sdk/src/main/java/com/_module.md) | module | This SDK implements multi-party Private Set Intersection (PSI) functionality, supporting ECDH and DH encryption protocols. It includes server/client components, data preprocessing tools, and a factory pattern. The core workflow consists of key generation, data encryption, and result comparison, with performance optimized through multithreading, making it suitable for secure data matching scenarios. |
| [mpc-common](mpc-common/src/main/java/com/_module.md) | module | AbstractHttpTransferVariable is an abstract class for handling HTTP requests, supporting JSON conversion and signature verification. The secure aggregation module implements key exchange and encrypted communication. The cryptography toolkit provides algorithms such as SM2/RSA. The MPC foundational toolkit supports numerical conversion and random data generation. The PSI module processes private set intersection queries. The local caching system adopts a two-tier structure. The DiffieHellmanKey class manages DH protocol parameters. The PIR module implements the private information retrieval protocol. The communication configuration class defines request parameters. |
| [mpc-pir](mpc-pir/mpc-pir-sdk/src/main/java/com/_module.md) | module | This module implements the Private Information Retrieval (PIR) protocol, including key generation, random number verification, and encrypted data transmission. It supports the Naor-Pinkas and Hauck protocols, provides synchronous/asynchronous interfaces, and involves data obfuscation, parameter validation, and secure transmission. It relies on cryptographic libraries and thread pools, making it suitable for hierarchical private query scenarios. |


