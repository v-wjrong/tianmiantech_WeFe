# Basic Information

|      |      |
|------|------|
| Name | mpc-sa |
| Language | .java |
| Code Path | WeFe/mpc/mpc-sa |
| Package Name | docs.mpc.mpc-sa |
| Brief Description | This module implements query processing and key exchange functionalities in secure multi-party computation, supporting differential privacy and cache management. It includes fixed/custom factor queries and DH key generation interfaces, relies on a caching system, and is suitable for scenarios such as federated learning. |

# Description

## Overview  
The core responsibility of this module is to achieve privacy-preserving data transmission and key exchange in secure multi-party computation, integrating query result processing, Diffie-Hellman key negotiation, and HTTP aggregate query functionalities. The unified interface specification includes two categories: key exchange interfaces (e.g., `queryDiffieHellmanKey`) adopt a TLS handshake-like mode, while result query interfaces (e.g., `queryResult`) support fixed/custom factor processing. Key data structures include Diffie-Hellman value lists, hexadecimal parameters p/g, UUID response objects, and request/response bodies (e.g., `QuerySAResultRequest`). External dependencies involve cache systems (e.g., CacheOperationFactory) and HTTP service configurations (e.g., ServerConfig). For instance, the `SecureAggregation` class implements secure aggregation through UUID management, while `QueryResultService` leverages random seeds to achieve differential privacy.

## Key Business Scenarios  
The module supports a typical two-phase workflow: first negotiating keys via the Diffie-Hellman protocol (similar to RPC calls), then initiating obfuscated result queries (resembling an event bus pattern). Complete functionalities cover key generation, parameter validation, cache read/write, and result accumulation, making it suitable for scenarios like federated learning. Interactions employ synchronous HTTP calls—for example, the client requests a public key, and the server responds with a 1024-bit random key, or aggregates data via ADD/SUB operations. APIs are divided into key exchange (requiring p/g parameters) and result query (supporting weight configuration) categories, with exception handling ensuring reliability. Specific implementations include `SecureAggregation` traversing server configurations to initiate requests and `QueryDiffieHellmanKeyService` enforcing hexadecimal data conversion for security.


### Package Internal Structure View

None

# File List

| Name   | Type  | Description |
|-------|------|-------------|
| [mpc-sa-sdk](mpc-sa-sdk/src/main/java/com/_module.md) | module | This module enables secure data transmission via the HTTP protocol, supporting Diffie-Hellman key exchange and result query, making it suitable for scenarios such as federated learning. Core interfaces include key negotiation and result retrieval, relying on HTTP server configuration. |
| [mpc-sa-server](mpc-sa-server/src/main/java/com/_module.md) | module | The QueryResultService processes query requests, providing two handle methods that involve cache retrieval, encryption computation, and result adjustment, returning the processed result and UUID. The QueryDiffieHellmanKeyService handles key exchange requests, generates random keys, performs encryption computation and caching, and returns the encrypted result and UUID. |


