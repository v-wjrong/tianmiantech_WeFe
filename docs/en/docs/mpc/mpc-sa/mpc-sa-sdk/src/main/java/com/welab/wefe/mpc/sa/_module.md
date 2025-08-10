# Basic Information

|      |      |
|------|------|
| Name | sa |
| Language | .java |
| Code Path | WeFe/mpc/mpc-sa/mpc-sa-sdk/src/main/java/com/welab/wefe/mpc/sa |
| Package Name | docs.mpc.mpc-sa.mpc-sa-sdk.src.main.java.com.welab.wefe.mpc.sa |
| Brief Description | This module enables secure data transmission via the HTTP protocol, supporting Diffie-Hellman key exchange and result querying, making it suitable for scenarios such as federated learning. Core interfaces include key negotiation and result retrieval, dependent on HTTP server configuration. |

# Description

## Overview  
This module implements privacy-preserving data transmission in secure multi-party computation, ensuring communication security through Diffie-Hellman key exchange and HTTP aggregated queries. The unified interface includes `queryDiffieHellmanKey` (key negotiation) and `queryResult` (result retrieval), adopting an RPC-like request-response pattern. The core data structures are `QueryDiffieHellmanKeyRequest/Response` and `QuerySAResultRequest/Response`, with external dependencies limited to HTTP server configuration (e.g., `ServerConfig`). For instance, the `SecureAggregation` class achieves secure aggregation via UUID and key management, while `ServerConfig` defines parameters such as service URLs and operation types.  

## Key Business Scenarios  
The typical workflow consists of two phases: first negotiating keys via the Diffie-Hellman protocol, then initiating obfuscated result queries. Interactions employ synchronous HTTP calls, such as a client requesting a public key followed by a server response. The functionality fully supports scenarios like federated learning, with the `SecureAggregation` class demonstrating a complete implementation: iterating through server configurations to initiate key requests, then collecting and accumulating computation results for return. The API provides query-oriented interfaces, supporting ADD/SUB operations and weight configuration, with exception handling ensuring reliability.


### Package Internal Structure View

```mermaid
graph TD
    sa --> sdk
    sdk --> transfer
    sdk --> SecureAggregation.java
    sdk --> config
    transfer --> impl
    transfer --> SecureAggregationTransferVariable.java
    impl --> HttpTransferVariable.java
    config --> ServerConfig.java
```

This flowchart illustrates the hierarchical structure of the MPC Secure Aggregation SDK. The root node "sa" contains the "sdk" module, which is further divided into the transfer module, main class (SecureAggregation.java), and configuration module (config). The transfer module includes implementation classes (impl) and interface classes, while the configuration module contains the server configuration class. The entire structure clearly demonstrates the dependency relationships between the SDK components.

# File List

| Name   | Type  | Description |
|-------|------|-------------|
| [sdk](sdk/_module.md) | package | This module enables secure data transmission via the HTTP protocol, supporting Diffie-Hellman key exchange and result query, making it suitable for scenarios such as federated learning. Core interfaces include key negotiation and result retrieval, dependent on HTTP server configuration. |


