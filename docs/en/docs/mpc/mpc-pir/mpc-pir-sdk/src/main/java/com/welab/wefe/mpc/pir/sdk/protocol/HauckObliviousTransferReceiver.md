# Basic Information

|      |      |
|------|------|
| Name | HauckObliviousTransferReceiver |
| Language | .java |
| Code Path | WeFe/mpc/mpc-pir/mpc-pir-sdk/src/main/java/com/welab/wefe/mpc/pir/sdk/protocol/HauckObliviousTransferReceiver.java |
| Package Name | com.welab.wefe.mpc.pir.sdk.protocol |
| Dependencies | ['java.math.BigInteger', 'java.util.ArrayList', 'java.util.List', 'java.util.concurrent.CompletableFuture', 'java.util.concurrent.ExecutionException', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'com.welab.wefe.mpc.commom.Conversion', 'com.welab.wefe.mpc.pir.protocol.nt.group.GroupArithmetic', 'com.welab.wefe.mpc.pir.protocol.nt.group.GroupElement', 'com.welab.wefe.mpc.pir.protocol.ot.ObliviousTransfer', 'com.welab.wefe.mpc.pir.protocol.ot.ObliviousTransferKey', 'com.welab.wefe.mpc.pir.protocol.ot.hauck.HauckObliviousTransfer', 'com.welab.wefe.mpc.pir.request.QueryRandomLegalRequest', 'com.welab.wefe.mpc.pir.request.QueryRandomLegalResponse', 'com.welab.wefe.mpc.pir.request.QueryRandomRequest', 'com.welab.wefe.mpc.pir.sdk.trasfer.PrivateInformationRetrievalTransferVariable', 'com.welab.wefe.mpc.util.EncryptUtil', 'cn.hutool.core.util.StrUtil'] |
| Brief Description | The `HauckObliviousTransferReceiver` class implements the `ObliviousTransfer` interface and is responsible for key derivation. By generating a random number `x` and verifying the validity of `s`, it calculates `r` and `xs`, ultimately generating the target key. It includes asynchronous operations and error handling. |

# Description

The `HauckObliviousTransferReceiver` class implements the `ObliviousTransfer` interface and is responsible for executing the receiver logic of the oblivious transfer protocol. This class includes attributes such as a UUID identifier, transfer variables, and an initial value `S`. The core method `keyDerivation` completes key derivation through steps such as generating a random number `x`, validating the legality of `S`, computing the values of `R` and `XS`, initializing the MAC, and generating the target key. The process employs asynchronous computation and legality verification mechanisms, ultimately returning an `ObliviousTransferKey` list containing the target key and results. Auxiliary methods include operations such as sending the `R` value, computing the `R` value, and checking the legality of `S`.

# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| HauckObliviousTransferReceiver | class | The `HauckObliviousTransferReceiver` class implements the `ObliviousTransfer` interface and is responsible for key derivation. By generating a random number `x` and verifying the validity of `s`, it calculates `r` and `xs` to ultimately generate the target key. It includes asynchronous computation and error handling logic. |



## Class HauckObliviousTransferReceiver

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | HauckObliviousTransferReceiver |
| Description | The `HauckObliviousTransferReceiver` class implements the `ObliviousTransfer` interface and is responsible for key derivation. By generating a random number `x` and verifying the validity of `s`, it calculates `r` and `xs` to ultimately generate the target key. It includes asynchronous computation and error handling logic. |


### UML Class Diagram

```mermaid
classDiagram
    class HauckObliviousTransfer {
        <<Abstract>>
        +String uuid
        +GroupArithmetic arithmetic
        +HauckObliviousTransfer(String uuid)
    }

    class ObliviousTransfer {
        <<Interface>>
        +List~ObliviousTransferKey~ keyDerivation(int target)
    }

    class HauckObliviousTransferReceiver {
        -Logger LOG
        -PrivateInformationRetrievalTransferVariable mTransferVariable
        -String firstS
        +HauckObliviousTransferReceiver(String uuid)
        +HauckObliviousTransferReceiver(String uuid, String s, PrivateInformationRetrievalTransferVariable transferVariable)
        +List~ObliviousTransferKey~ keyDerivation(int target)
        -QueryRandomLegalResponse sendR(GroupElement r, int attemptCount)
        -GroupElement calcR(GroupArithmetic arithmetic, int target, BigInteger x, GroupElement s)
        -boolean checkSLegal(GroupElement s)
    }

    class PrivateInformationRetrievalTransferVariable {
        <<Interface>>
        +QueryRandomResponse queryRandom(QueryRandomRequest request)
        +QueryRandomLegalResponse queryRandomLegal(QueryRandomLegalRequest request)
    }

    class QueryRandomRequest {
        -String uuid
        -int attemptCount
        +setUuid(String uuid)
        +setAttemptCount(int attemptCount)
        +getS() String
    }

    class QueryRandomLegalRequest {
        -String uuid
        -boolean sLegal
        -int attemptCount
        -String r
        +setUuid(String uuid)
        +setsLegal(boolean sLegal)
        +setAttemptCount(int attemptCount)
        +setR(String r)
    }

    class QueryRandomLegalResponse {
        -List~String~ results
        +getResults() List~String~
    }

    class ObliviousTransferKey {
        -int target
        -byte[] key
        -String result
        +ObliviousTransferKey(int target, byte[] key)
        +setResult(String result)
    }

    HauckObliviousTransferReceiver --|> HauckObliviousTransfer
    HauckObliviousTransferReceiver ..|> ObliviousTransfer
    HauckObliviousTransferReceiver --> PrivateInformationRetrievalTransferVariable : depends
    HauckObliviousTransferReceiver --> QueryRandomRequest : uses
    HauckObliviousTransferReceiver --> QueryRandomLegalRequest : uses
    HauckObliviousTransferReceiver --> QueryRandomLegalResponse : uses
    HauckObliviousTransferReceiver --> ObliviousTransferKey : creates
    PrivateInformationRetrievalTransferVariable <.. QueryRandomRequest : processes
    PrivateInformationRetrievalTransferVariable <.. QueryRandomLegalRequest : processes
    PrivateInformationRetrievalTransferVariable ..> QueryRandomLegalResponse : returns
```

This code describes an implementation of a receiver for oblivious transfer based on the Hauck protocol, which inherits from the abstract class HauckObliviousTransfer and implements the ObliviousTransfer interface. The core functionality involves generating target keys through the keyDerivation method, encompassing operations such as random number generation, group arithmetic, legality checks, and asynchronous communication. The class diagram illustrates the interaction between the receiver and the transfer variable interface, request-response objects, as well as the data flow during the key generation process.


### Internal Method Call Graph

```mermaid
graph TD
    A["Class HauckObliviousTransferReceiver"]
    B["Attribute: Logger LOG"]
    C["Attribute: PrivateInformationRetrievalTransferVariable mTransferVariable"]
    D["Attribute: String firstS"]
    E["Constructor 1: HauckObliviousTransferReceiver(String uuid)"]
    F["Constructor 2: HauckObliviousTransferReceiver(String uuid, String s, PrivateInformationRetrievalTransferVariable transferVariable)"]
    G["Overridden Method: List<ObliviousTransferKey> keyDerivation(int target)"]
    H["Private Method: QueryRandomLegalResponse sendR(GroupElement r, int attemptCount)"]
    I["Private Method: GroupElement calcR(GroupArithmetic arithmetic, int target, BigInteger x, GroupElement s)"]
    J["Private Method: boolean checkSLegal(GroupElement s)"]

    A --> B
    A --> C
    A --> D
    A --> E
    A --> F
    A --> G
    A --> H
    A --> I
    A --> J
```

```mermaid
sequenceDiagram
    participant A as keyDerivation
    participant B as genRandomScalar
    participant C as getGroupElement
    participant D as checkSLegal
    participant E as calcR
    participant F as arithmetic.mul
    participant G as CompletableFuture
    participant H as initMac
    participant I as macTecElement
    participant J as sendR

    A->>B: Generate random x
    loop Validity Check Loop
        A->>C: Get GroupElement s
        A->>D: Verify s validity
        alt Invalid
            A->>J: Send invalid s notification
        end
    end
    A->>E: Async compute r
    A->>F: Async compute xs
    A->>G: Await async results
    A->>H: Initialize MAC
    A->>I: Generate target key
    A->>J: Send valid r value
    A->>A: Assemble return key list
```

This flowchart illustrates the core structure and interaction process of the HauckObliviousTransferReceiver class. Inheriting from HauckObliviousTransfer and implementing the ObliviousTransfer interface, the class contains attributes like logger and transfer variables, along with the key derivation method. The sequence diagram details the execution flow of the keyDerivation method: starting from random number generation, verifying parameter validity through loops, leveraging asynchronous computation for performance, and ultimately completing key derivation and result return. The entire process involves multiple cryptographic operations and thread coordination, reflecting the core processing logic of secure transfer protocols.

### Field List

| Name  | Type  | Description |
|-------|-------|------|
| mTransferVariable | PrivateInformationRetrievalTransferVariable | Private Information Retrieval Transfer Variable mTransferVariable. |
| firstS | String | Declare a string variable firstS. |
| LOG = LoggerFactory.getLogger(HauckObliviousTransferReceiver.class) | Logger | The `HauckObliviousTransferReceiver` class defines a private static logger instance named `LOG`. |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| sendR | QueryRandomLegalResponse | The method sendR sends a random legitimate request, sets the UUID, legitimate flag, attempt count, and R value, returns the query result, and logs the record. |
| keyDerivation | List<ObliviousTransferKey> | Method to Generate ObliviousTransferKey: Generate a random number x, iteratively obtain a valid s, asynchronously compute r and xs, initialize the mac, and generate the key, finally returning a key list containing the results. |
| calcR | GroupElement | The method calcR computes the group element r. The process involves: generating t via hashing, computing ct=c*t and xg=x*generator, and finally r=ct+xg. Logging marks the start and end. |
| checkSLegal | boolean | Check whether the GroupElement object s is within the arithmetic group, returning a boolean value. |




