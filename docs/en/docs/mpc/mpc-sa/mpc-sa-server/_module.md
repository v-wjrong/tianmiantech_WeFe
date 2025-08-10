# Basic Information

|      |      |
|------|------|
| Name | mpc-sa-server |
| Language | .java |
| Code Path | WeFe/mpc/mpc-sa/mpc-sa-server |
| Package Name | docs.mpc.mpc-sa.mpc-sa-server |
| Brief Description | The QueryResultService processes query requests, providing two handle methods that involve cache retrieval, encryption computation, and result adjustment, returning the processed result and UUID. The QueryDiffieHellmanKeyService handles key exchange requests, generates random keys, performs encryption computation and caching, and returns the encrypted result and UUID. |

# Description

## Overview  
The core responsibility of this module is to implement query result processing in secure multi-party computation and Diffie-Hellman key exchange functionality, including cryptographic computations and cache management. The interface specifications encompass two methods for query result processing (fixed factor and custom factor) as well as key generation and encryption interfaces. Key data structures involve the DiffieHellman value list, hexadecimal parameters p/g, and UUID response objects. External dependencies primarily include the cache system (e.g., CacheOperationFactory). For instance, QueryResultService achieves differential privacy by skipping the current index item, while QueryDiffieHellmanKeyService ensures security using 1024-bit random keys.  

## Primary Business Scenarios  
The module supports two typical workflows: query result processing resembles an event bus pattern, where results are accumulated by adjusting signs and random seeds; the key exchange process is similar to a TLS handshake, generating random keys and performing encryption based on p/g parameters. Complete functionalities include cache read/write, parameter validation, cryptographic operations, and response construction. For example, when processing queries, the current index is automatically skipped, and during key exchange, hexadecimal data is forcibly converted. API types cover two integration scenarios: result queries (with factor parameters) and key generation (requiring p/g parameters).


### Package Internal Structure View

None

# File List

| Name   | Type  | Description |
|-------|------|-------------|
| [com](src/main/java/com/_module.md) | folder | The QueryResultService processes query requests, providing two handle methods that involve cache retrieval, encryption computation, and result adjustment, returning the processed result and UUID. The QueryDiffieHellmanKeyService handles key exchange requests, generates random keys, performs encryption computation and caching, and returns the encrypted result and UUID. |


