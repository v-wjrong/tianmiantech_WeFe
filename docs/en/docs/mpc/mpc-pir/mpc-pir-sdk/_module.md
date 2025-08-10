# Basic Information

|      |      |
|------|------|
| Name | mpc-pir-sdk |
| Language | .java |
| Code Path | WeFe/mpc/mpc-pir/mpc-pir-sdk |
| Package Name | docs.mpc.mpc-pir.mpc-pir-sdk |
| Brief Description | This module implements secure private information retrieval based on the Naor-Pinkas protocol, including data obfuscation, OT interaction, and encrypted query functionality. Core classes handle key generation, parameter validation, and result decryption, supporting client-server secure retrieval workflows. It provides obfuscation interfaces to generate differentiated instances, with configuration classes validating parameter legality. The system ensures query privacy and process security as a whole. |

# Description

## Overview  
The core responsibility of this module is to implement secure Private Information Retrieval (PIR) functionality. Based on the Naor-Pinkas and Hauck oblivious transfer protocols, it ensures query privacy through data obfuscation and encrypted transmission. The interface specifications are divided into two categories: basic PIR interfaces (e.g., generate/query) handle data preparation and retrieval, while protocol-specific interfaces (e.g., queryNaorPinkasRandom) manage encrypted parameter exchanges. Key data structures include transmission objects such as QueryKeysRequest and ObliviousTransferKey, as well as PrivateInformationRetrievalConfig, which contains primary key lists and obfuscation parameters. External dependencies involve the foundational communication framework and utility classes like RandomPhoneNum. For example, the NaorPinkasQuery class implements the Diffie-Hellman encryption process with 1024-bit keys.

## Main Business Scenarios  
A typical application is the client-server secure retrieval process: first, generateConfuse is used to create an obfuscated dataset, followed by phased calls to protocol interfaces to complete encrypted transmission, and finally decrypt the target result. The interaction resembles a two-phase commit protocol, supporting both Naor-Pinkas and Hauck OT modes. For instance, HauckObliviousTransferReceiver ensures transmission security through MAC verification and key derivation. The full functionality covers the entire lifecycle from data obfuscation (e.g., MD5 encryption of phone numbers) and parameter validation to secure retrieval, with exception handling integrated throughout all stages. API integration examples include anonymous queries and compliance check scenarios.


### Package Internal Structure View

None

# File List

| Name   | Type  | Description |
|-------|------|-------------|
| [com](src/main/java/com/_module.md) | folder | This module implements secure private information retrieval based on the Naor-Pinkas protocol, including data obfuscation, OT interaction, and encrypted query functionality. Core classes handle key generation, parameter validation, and result decryption, supporting client-server secure retrieval workflows. It provides obfuscation interfaces to generate differentiated instances, with configuration classes validating parameter legitimacy. The system ensures query privacy and process security as a whole. |


