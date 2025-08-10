# Basic Information

|      |      |
|------|------|
| Name | wefe |
| Language | .java |
| Code Path | WeFe/mpc/mpc-sa/mpc-sa-server/src/main/java/com/welab/wefe |
| Package Name | docs.mpc.mpc-sa.mpc-sa-server.src.main.java.com.welab.wefe |
| Brief Description | The QueryResultService processes query requests, providing two handle methods that involve cache retrieval, encryption computation, and result adjustment, returning the processed result and UUID. The QueryDiffieHellmanKeyService handles key exchange requests, generates random keys, performs encryption computation and caching, and returns the encrypted result and UUID. |

# Description

## Overview  
The core responsibility of this module is to implement query result processing in secure multi-party computation and Diffie-Hellman key exchange functionality, including cryptographic computations and cache management. The interface specifications encompass two query result processing methods (fixed factor and custom factor) as well as key generation and encryption interfaces. Key data structures involve DiffieHellman value lists, hexadecimal parameters p/g, and UUID response objects. External dependencies primarily include the cache system (e.g., CacheOperationFactory). For instance, QueryResultService achieves differential privacy by skipping the current index item, while QueryDiffieHellmanKeyService ensures security using 1024-bit random keys.  

## Key Business Scenarios  
The module supports two typical workflows: query result processing resembles an event bus pattern, adjusting signs and accumulating results with random seeds; the key exchange process is similar to TLS handshake, generating random keys and performing encryption based on p/g parameters. Complete functionalities include cache read/write, parameter validation, cryptographic operations, and response construction. For example, during query processing, the current index is automatically skipped, while key exchange enforces hexadecimal data conversion. API types cover two integration scenarios: result queries (with factor parameters) and key generation (requiring p/g parameters).


### Package Internal Structure View

```mermaid
graph TD
    wefe --> mpc
    mpc --> sa
    sa --> server
    server --> service
    service --> QueryResultService.java
    service --> QueryDiffieHellmanKeyService.java
```

This flowchart illustrates the server-side code hierarchy of the MPC secure computation module in the WeFe project. Starting from the root directory 'wefe', it sequentially traverses through the 'mpc', 'sa', and 'server' layers, ultimately reaching the 'service' layer, which contains two service class files: QueryResultService and QueryDiffieHellmanKeyService. The entire structure presents a clear tree-like dependency relationship, involving a total of 7 path nodes.

# File List

| Name   | Type  | Description |
|-------|------|-------------|
| [mpc](mpc/_module.md) | package | The QueryResultService handles query requests, providing two handle methods that involve cache retrieval, encryption computation, and result adjustment, returning processed results and UUID. The QueryDiffieHellmanKeyService processes key exchange requests, generates random keys, performs encryption computation and caching, and returns encrypted results and UUID. |


