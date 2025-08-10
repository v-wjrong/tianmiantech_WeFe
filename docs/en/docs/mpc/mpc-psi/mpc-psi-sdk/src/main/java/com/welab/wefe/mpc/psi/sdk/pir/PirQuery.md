# Basic Information

|      |      |
|------|------|
| Name | PirQuery |
| Language | .java |
| Code Path | WeFe/mpc/mpc-psi/mpc-psi-sdk/src/main/java/com/welab/wefe/mpc/psi/sdk/pir/PirQuery.java |
| Package Name | com.welab.wefe.mpc.psi.sdk.pir |
| Dependencies | ['java.math.BigInteger', 'java.util.List', 'java.util.UUID', 'com.welab.wefe.mpc.commom.Constants', 'com.welab.wefe.mpc.config.CommunicationConfig', 'com.welab.wefe.mpc.pir.protocol.ro.hf.HashFunction', 'com.welab.wefe.mpc.pir.protocol.ro.hf.Sha256', 'com.welab.wefe.mpc.pir.request.QueryKeysRequest', 'com.welab.wefe.mpc.pir.request.naor.QueryNaorPinkasRandomResponse', 'com.welab.wefe.mpc.pir.request.naor.QueryNaorPinkasResultRequest', 'com.welab.wefe.mpc.pir.request.naor.QueryNaorPinkasResultResponse', 'com.welab.wefe.mpc.psi.sdk.service.PrivateSetIntersectionService', 'com.welab.wefe.mpc.util.DiffieHellmanUtil', 'com.welab.wefe.mpc.util.EncryptUtil'] |
| Brief Description | The PirQuery class implements private information retrieval using the NaorPinkas OT method, generating random keys to process query requests and employing Diffie-Hellman encryption along with AES decryption to return the target index result. |

# Description

The `query` method in the `PirQuery` class implements private information retrieval functionality based on the Naor-Pinkas oblivious transfer protocol. This method takes the target index, a list of IDs, and communication configuration parameters as input. It first generates a random key `k`, constructs a random query request, and retrieves the response. After validating the response, it extracts the UUID, Diffie-Hellman parameters `g`, `p`, and `secret`. It then computes the public key `pk`, processes the parameters related to the target index, and constructs the result query request. Upon receiving the response, it uses SHA256 hashing and AES decryption to ultimately return the decrypted result corresponding to the target index. The entire process involves Diffie-Hellman key exchange, hash computation, and symmetric encryption operations.

# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| PirQuery | class | The PirQuery class implements private information retrieval functionality, securely querying target index data through Diffie-Hellman key exchange and AES encryption. It includes steps such as random request generation, key computation, and result decryption. |



## Class PirQuery

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | PirQuery |
| Description | The PirQuery class implements private information retrieval functionality, securely querying target index data through Diffie-Hellman key exchange and AES encryption. It includes steps such as random request generation, key computation, and result decryption. |


### UML Class Diagram

```mermaid
classDiagram
    class PirQuery {
        +query(int targetIndex, List~Object~ ids, CommunicationConfig communicationConfig) String
    }

    class DiffieHellmanUtil {
        <<Utility>>
        +generateRandomKey(int bitLength) BigInteger
        +hexStringToBigInteger(String hex) BigInteger
        +encrypt(BigInteger g, BigInteger k, BigInteger p) BigInteger
        +modDivide(BigInteger c, BigInteger pk, BigInteger p) BigInteger
        +bigIntegerToHexString(BigInteger num) String
    }

    class QueryKeysRequest {
        -List~Object~ ids
        -String otMethod
        -String requestId
        +setIds(List~Object~ ids)
        +setOtMethod(String method)
        +setRequestId(String id)
    }

    class PrivateSetIntersectionService {
        +handlePirResult(CommunicationConfig config, QueryKeysRequest request) QueryNaorPinkasRandomResponse
        +queryNaorPinkasResult(CommunicationConfig config, QueryNaorPinkasResultRequest request) QueryNaorPinkasResultResponse
    }

    class QueryNaorPinkasRandomResponse {
        -int code
        -String message
        -String uuid
        -String g
        -String p
        -String secret
        -List~String~ randoms
        +getCode() int
        +getMessage() String
        +getUuid() String
        +getG() String
        +getP() String
        +getSecret() String
        +getRandoms() List~String~
    }

    class QueryNaorPinkasResultRequest {
        -String uuid
        -String pk
        +setUuid(String uuid)
        +setPk(String pk)
    }

    class QueryNaorPinkasResultResponse {
        -int code
        -String message
        -List~String~ encryptResults
        +getCode() int
        +getMessage() String
        +getEncryptResults() List~String~
    }

    class EncryptUtil {
        <<Utility>>
        +decryptByAES(String encrypted, byte[] key) String
    }

    class HashFunction {
        <<Interface>>
        +digest(byte[] input) byte[]
    }

    class Sha256 {
        +digest(byte[] input) byte[]
    }

    PirQuery --> DiffieHellmanUtil : Dependency
    PirQuery --> QueryKeysRequest : Create
    PirQuery --> PrivateSetIntersectionService : Create
    PirQuery --> QueryNaorPinkasRandomResponse : Use
    PirQuery --> QueryNaorPinkasResultRequest : Create
    PirQuery --> QueryNaorPinkasResultResponse : Use
    PirQuery --> EncryptUtil : Dependency
    PirQuery --> HashFunction : Dependency
    Sha256 ..|> HashFunction : Implements
    PrivateSetIntersectionService --> QueryKeysRequest : Process
    PrivateSetIntersectionService --> QueryNaorPinkasResultRequest : Process
```

This code demonstrates the implementation flow of a Private Information Retrieval (PIR) query, primarily involving Diffie-Hellman key exchange, Naor-Pinkas oblivious transfer protocol, and AES encryption/decryption processes. The core class PirQuery coordinates multiple utility and service classes to complete secure queries, including key generation, encryption computation, request handling, and result decryption. The class diagram clearly illustrates dependencies between components, particularly interactions between encryption utility classes and service classes, as well as the inheritance relationship between the HashFunction interface and its implementation class Sha256. The overall design reflects a modular secure computation workflow.


### Internal Method Call Graph

```mermaid
graph TD
    A["Query Method Entry"]
    B["Generate Random Key k: DiffieHellmanUtil.generateRandomKey"]
    C["Create QueryKeysRequest Object and Set Parameters"]
    D["Create PrivateSetIntersectionService Instance"]
    E["Call handlePirResult to Obtain randomResponse"]
    F{"randomResponse.getCode() != 0?"}
    G["Throw Exception: randomResponse.getMessage()"]
    H["Parse Response Parameters: uuid/g/p/secret"]
    I["Calculate pk: DiffieHellmanUtil.encrypt"]
    J{"targetIndex != 0?"}
    K["Adjust pk Value: DiffieHellmanUtil.modDivide"]
    L["Create QueryNaorPinkasResultRequest and Set Parameters"]
    M["Call queryNaorPinkasResult to Obtain response"]
    N{"response.getCode() != 0?"}
    O["Throw Exception: response.getMessage()"]
    P["Generate AES Key: hash.digest+DiffieHellmanUtil.encrypt"]
    Q["Return Decrypted Result: EncryptUtil.decryptByAES"]

    A --> B
    B --> C
    C --> D
    D --> E
    E --> F
    F -- Yes --> G
    F -- No --> H
    H --> I
    I --> J
    J -- Yes --> K
    K --> L
    J -- No --> L
    L --> M
    M --> N
    N -- Yes --> O
    N -- No --> P
    P --> Q
```

This flowchart illustrates the complete PIR query process: First, generate a random key and create an initial request, then validate the status code after obtaining the response via the service. If successful, parse the parameters and calculate the encrypted value, adjust parameters based on the target index, and initiate the final query request. Finally, generate an AES key to decrypt the result at the specified index. The entire process involves two service calls and multiple encryption operations, rigorously handling error conditions and conditional branches.

### Field List

| Name  | Type  | Description |
|-------|-------|------|

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| query | String | This method queries the target index data through the Naor-Pinkas oblivious transfer protocol, generates a random key to process the request, and decrypts the returned result after verifying the response. |




