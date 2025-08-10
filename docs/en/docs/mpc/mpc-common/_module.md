# Basic Information

|      |      |
|------|------|
| Name | mpc-common |
| Language | .java |
| Code Path | WeFe/mpc/mpc-common |
| Package Name | docs.mpc.mpc-common |
| Brief Description | AbstractHttpTransferVariable is an abstract class for handling HTTP requests, supporting JSON conversion and signature verification. The secure aggregation module implements key exchange and encrypted communication. The cryptography toolkit provides algorithms such as SM2/RSA. The MPC foundational toolkit supports numerical conversion and random data generation. The PSI module processes private set intersection queries. The local caching system adopts a two-tier structure. The DiffieHellmanKey class manages DH protocol parameters. The PIR module implements the private information retrieval protocol. The communication configuration class defines request parameters. |

# Description

## Overview  
This module serves as the foundational framework for Secure Multi-party Computation (MPC), with its core responsibilities encompassing cryptographic protocol encapsulation, key management, and secure communication, akin to a middleware layer in a zero-trust architecture. The interface specifications comprise four categories: Secure Aggregation (QuerySAResult), Key Exchange (QueryDiffieHellmanKey), PSI Query (QueryPrivateSetIntersection), and PIR Protocol (QueryKeysRequest), all utilizing POJO + JSON serialization. Key data structures include Diffie-Hellman parameters (p/g), PSI batch control fields, PIR session identifiers (uuid), and group operation coordinates, relying on BouncyCastle/JCE cryptographic libraries and JSON utilities. For instance, SM2KeyPair manages national cryptographic keys, while LocalIntermediateCache implements thread-safe storage.  

## Primary Business Scenarios  
The module supports federated learning and joint risk control scenarios, with a typical workflow as follows: 1) DH key exchange → 2) secure data aggregation/PSI comparison → 3) PIR privacy retrieval. Interactions adopt a request-response chain model, correlating sessions via uuid, similar to an encrypted envelope mechanism. Functional completeness is reflected in: support for SM2/RSA signatures, AES/SHA encryption, Naor-Pinkas protocols, and weight-adjusted aggregation. For example, SignUtil automatically selects algorithms, while CacheUtil manages temporary data. API types are hierarchically designed, with foundational layers such as DiffieHellmanUtil static methods and protocol layers like QuerySAResultRequest object-oriented operations. Integration cases include cross-institution ID secure matching and encrypted phone number generation.


### Package Internal Structure View

None

# File List

| Name   | Type  | Description |
|-------|------|-------------|
| [com](src/main/java/com/_module.md) | folder | AbstractHttpTransferVariable is an abstract class for handling HTTP requests, supporting JSON conversion and signature verification. The secure aggregation module implements key exchange and encrypted communication. The cryptography toolkit provides algorithms such as SM2/RSA. The MPC foundational toolkit supports numerical conversion and random data generation. The PSI module processes private set intersection queries. The local caching system adopts a two-tier structure. The DiffieHellmanKey class manages DH protocol parameters. The PIR module implements the private information retrieval protocol. The communication configuration class defines request parameters. |


