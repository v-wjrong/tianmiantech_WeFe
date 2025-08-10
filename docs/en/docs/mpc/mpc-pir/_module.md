# Basic Information

|      |      |
|------|------|
| Name | mpc-pir |
| Language | .java |
| Code Path | WeFe/mpc/mpc-pir |
| Package Name | docs.mpc.mpc-pir |
| Brief Description | This module implements the Private Information Retrieval (PIR) protocol, including key generation, random number verification, and encrypted data transmission. It supports the Naor-Pinkas and Hauck protocols, provides synchronous/asynchronous interfaces, and involves data obfuscation, parameter validation, and secure transmission. It relies on cryptographic libraries and thread pools, making it suitable for hierarchical private query scenarios. |

# Description

## Overview  
This module implements the Private Information Retrieval (PIR) functionality in secure multi-party computation, with its core responsibility being to ensure query privacy through the Naor-Pinkas and Hauck oblivious transfer protocols, combined with data obfuscation and encrypted transmission to achieve a secure middleware pattern. The unified interface specification includes six types of operations: basic PIR interfaces (e.g., generate/query), protocol-specific interfaces (e.g., queryNaorPinkasRandom), random number processing, key derivation, and more. Key data structures are aggregated into five categories: transfer objects (QueryKeysRequest/ObliviousTransferKey), configuration parameters (PrivateInformationRetrievalConfig), encryption parameters (Diffie-Hellman key pairs/AES keys), cache objects (HauckTarget), and tracking identifiers (UUID). External dependencies include the JCE encryption library, thread pools, communication frameworks, and utility classes (e.g., RandomPhoneNum). For instance, thread-safe caching is implemented via ArrayBlockingQueue, and a 1024-bit Diffie-Hellman key exchange process is employed.

## Key Business Scenarios  
A typical application is the hierarchical secure retrieval process: the preprocessing stage generates obfuscated datasets (e.g., MD5-encrypted phone numbers), while the query stage combines the Naor-Pinkas/Hauck protocols to complete encrypted transmission, resembling a two-phase commit protocol. The complete business process spans three dimensions: 1) cache control (500-capacity threshold + 2-second sleep detection), 2) security validation (120-second timeout + MAC verification), and 3) asynchronous transmission (JSON result encapsulation). The interaction mode supports a dual-track API: synchronous interfaces handle immediate requests (e.g., getHauckTarget), while asynchronous services manage background tasks (e.g., HuackKeyService thread pool). For example, HauckObliviousTransferReceiver ensures transmission security through key derivation, and NaorPinkasResultService implements hybrid encryption gateway functionality. Functional integrity covers the entire lifecycle from data obfuscation and parameter validation to secure retrieval, with exception handling integrated throughout all stages.


### Package Internal Structure View

None

# File List

| Name   | Type  | Description |
|-------|------|-------------|
| [mpc-pir-sdk](mpc-pir-sdk/src/main/java/com/_module.md) | module | This module implements secure private information retrieval based on the Naor-Pinkas protocol, including data obfuscation, OT interaction, and encrypted query functionality. Core classes handle key generation, parameter validation, and result decryption, supporting client-server secure retrieval workflows. It provides obfuscation interfaces to generate differentiated instances, with configuration classes validating parameter legality. The system ensures query privacy and process security as a whole. |
| [mpc-pir-server](mpc-pir-server/src/main/java/com/_module.md) | module | The `PrivateInformationRetrievalEvent` class handles private information retrieval events, containing `uuid` and `keys` attributes. The module implements PIR protocol data transmission and verification, managing random numbers and encrypted data. The `ProduceHauckTargetThread` thread generates and caches `HauckTarget` objects. The `HauckObliviousTransferSender` class implements the key generation process. The module provides secure query services based on the Naor-Pinkas protocol. The `HauckTargetCache` singleton class manages thread-safe caching. The `PrivateInformationRetrievalFlowServer` class handles the retrieval process. The `PrivateInformationRetrievalServer` class provides server initialization and cache management functionality. |


