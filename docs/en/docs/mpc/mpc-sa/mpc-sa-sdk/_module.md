# Basic Information

|      |      |
|------|------|
| Name | mpc-sa-sdk |
| Language | .java |
| Code Path | WeFe/mpc/mpc-sa/mpc-sa-sdk |
| Package Name | docs.mpc.mpc-sa.mpc-sa-sdk |
| Brief Description | This module enables secure data transmission via the HTTP protocol, supporting Diffie-Hellman key exchange and result query, making it suitable for scenarios such as federated learning. Core interfaces include key negotiation and result retrieval, relying on HTTP server configuration. |

# Description

## Overview  
This module implements privacy-preserving data transmission in secure multi-party computation, ensuring communication security through Diffie-Hellman key exchange and HTTP aggregated queries. The unified interface includes `queryDiffieHellmanKey` (key negotiation) and `queryResult` (result retrieval), adopting an RPC-like request-response pattern. Core data structures are `QueryDiffieHellmanKeyRequest/Response` and `QuerySAResultRequest/Response`, with external dependencies limited to HTTP server configurations (e.g., `ServerConfig`). For instance, the `SecureAggregation` class implements secure aggregation via UUID and key management, while `ServerConfig` defines parameters such as service URLs and operation types.  

## Key Business Scenarios  
The typical workflow consists of two phases: first negotiating keys via the Diffie-Hellman protocol, then initiating obfuscated result queries. Interactions use synchronous HTTP calls, such as client requests for public keys followed by server responses. The functionality fully supports scenarios like federated learning, with the `SecureAggregation` class demonstrating a complete implementation: iterating through server configurations to initiate key requests before collecting and accumulating computation results for return. The API provides query-class interfaces, supporting ADD/SUB operations and weight configuration, with exception handling ensuring reliability.


### Package Internal Structure View

None

# File List

| Name   | Type  | Description |
|-------|------|-------------|
| [com](src/main/java/com/_module.md) | folder | This module enables secure data transmission via the HTTP protocol, supporting Diffie-Hellman key exchange and result queries, making it suitable for scenarios such as federated learning. Core interfaces include key negotiation and result retrieval, which depend on HTTP server configuration. |


