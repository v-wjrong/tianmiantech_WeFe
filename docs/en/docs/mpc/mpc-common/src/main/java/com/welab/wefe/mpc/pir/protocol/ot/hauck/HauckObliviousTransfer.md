# Basic Information

|      |      |
|------|------|
| Name | HauckObliviousTransfer |
| Language | .java |
| Code Path | WeFe/mpc/mpc-common/src/main/java/com/welab/wefe/mpc/pir/protocol/ot/hauck/HauckObliviousTransfer.java |
| Package Name | com.welab.wefe.mpc.pir.protocol.ot.hauck |
| Dependencies | ['com.welab.wefe.mpc.pir.protocol.nt.field.integers.IntegersModuloPrimeElement', 'com.welab.wefe.mpc.pir.protocol.nt.group.GroupArithmetic', 'com.welab.wefe.mpc.pir.protocol.nt.group.GroupElement', 'com.welab.wefe.mpc.pir.protocol.nt.group.cyclic.twisted.TwistedEdwardsCurveArithmetic', 'com.welab.wefe.mpc.pir.protocol.nt.group.cyclic.twisted.TwistedEdwardsCurveElement', 'com.welab.wefe.mpc.pir.protocol.ro.hf.HashFunction', 'com.welab.wefe.mpc.pir.protocol.ro.hf.Sha256', 'com.welab.wefe.mpc.pir.protocol.ro.mac.HashBasedMessageAuthenticationCode', 'com.welab.wefe.mpc.pir.protocol.ro.mac.Sha256MAC', 'java.math.BigInteger', 'java.security.SecureRandom'] |
| Brief Description | The HauckObliviousTransfer class implements an oblivious transfer protocol based on twisted Edwards curves, incorporating functionalities such as random number generation, hash computation, MAC initialization, and target generation. |

# Description

The `HauckObliviousTransfer` class implements an oblivious transfer protocol based on twisted Edwards curves. This class includes core components such as UUID identifiers, group operations, hash functions, and message authentication codes. The constructor initializes the curve arithmetic module and SHA-256 hash. It provides functionalities like generating random scalars, computing group element hashes, MAC initialization, and group element validation. The `generateHauckTarget` method continuously generates eligible transfer targets, containing a random scalar `y` along with its corresponding group element `s` and hash result `t`, ensuring `s` is within the group and the x-coordinate of `t` is valid. The entire class implements cryptographically secure foundational operations and the core logic of the protocol.

# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| HauckObliviousTransfer | class | The HauckObliviousTransfer class implements an oblivious transfer protocol based on twisted Edwards curves, incorporating functionalities for random number generation, hash computation, MAC initialization, and target generation. |



## Class HauckObliviousTransfer

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | HauckObliviousTransfer |
| Description | The HauckObliviousTransfer class implements an oblivious transfer protocol based on twisted Edwards curves, incorporating functionalities for random number generation, hash computation, MAC initialization, and target generation. |


### UML Class Diagram

```mermaid
classDiagram
    class HauckObliviousTransfer {
        +String uuid
        +GroupArithmetic arithmetic
        +HashFunction hash
        +HashBasedMessageAuthenticationCode mac
        +HauckObliviousTransfer(String uuid)
        +BigInteger genRandomScalar()
        +GroupElement hashTecElement(GroupElement element)
        +void initMac(GroupElement s, GroupElement r)
        +byte[] macTecElement(GroupElement element)
        +GroupElement getGroupElement(Object object)
        +HauckTarget generateHauckTarget()
    }

    class GroupArithmetic {
        <<Interface>>
        +BigInteger getFieldOrder()
        +GroupElement getGenerator()
        +byte[] encode(GroupElement element)
        +GroupElement decode(byte[] bytes)
        +GroupElement mul(BigInteger scalar, GroupElement element)
        +boolean isInGroup(GroupElement element)
    }

    class TwistedEdwardsCurveArithmetic {
        +TwistedEdwardsCurveArithmetic()
    }

    class HashFunction {
        <<Interface>>
        +byte[] digest(byte[] input)
    }

    class Sha256 {
        +Sha256()
    }

    class HashBasedMessageAuthenticationCode {
        <<Interface>>
        +byte[] digest(byte[] input)
    }

    class Sha256MAC {
        +Sha256MAC(byte[] key)
    }

    class GroupElement {
        <<Interface>>
    }

    class TwistedEdwardsCurveElement {
        +TwistedEdwardsCurveElement(IntegersModuloPrimeElement x, IntegersModuloPrimeElement y)
    }

    class IntegersModuloPrimeElement {
        +BigInteger val
        +IntegersModuloPrimeElement(BigInteger val)
    }

    class HauckTarget {
        +BigInteger y
        +GroupElement s
        +GroupElement t
        +HauckTarget(BigInteger y, GroupElement s, GroupElement t)
    }

    HauckObliviousTransfer --> GroupArithmetic : uses
    HauckObliviousTransfer --> HashFunction : uses
    HauckObliviousTransfer --> HashBasedMessageAuthenticationCode : uses
    TwistedEdwardsCurveArithmetic ..|> GroupArithmetic : implements
    Sha256 ..|> HashFunction : implements
    Sha256MAC ..|> HashBasedMessageAuthenticationCode : implements
    TwistedEdwardsCurveElement ..|> GroupElement : implements
}

This code describes a HauckObliviousTransfer class that implements an elliptic curve-based oblivious transfer protocol. The class contains core components such as UUID identifier, group arithmetic operator, hash function, and MAC authentication, providing functionalities like random scalar generation, group element hashing, MAC initialization and computation, group element conversion, and Hauck target generation. It implements group arithmetic using Twisted Edwards curves, employs SHA256 for hashing and MAC calculations, and follows cryptographic protocol design patterns with clear hierarchical structure through interface decoupling.


### Internal Method Call Graph

```mermaid
graph TD
    A["Class HauckObliviousTransfer"]
    B["Attribute: String uuid"]
    C["Attribute: GroupArithmetic arithmetic"]
    D["Attribute: HashFunction hash"]
    E["Attribute: HashBasedMessageAuthenticationCode mac"]
    F["Constructor: HauckObliviousTransfer(String uuid)"]
    G["Method: BigInteger genRandomScalar()"]
    H["Method: GroupElement hashTecElement(GroupElement element)"]
    I["Method: void initMac(GroupElement s, GroupElement r)"]
    J["Method: byte[] macTecElement(GroupElement element)"]
    K["Method: GroupElement getGroupElement(Object object)"]
    L["Method: HauckTarget generateHauckTarget()"]
    M["Internal call: new TwistedEdwardsCurveArithmetic()"]
    N["Internal call: new Sha256()"]
    O["Internal call: arithmetic.getFieldOrder()"]
    P["Internal call: new SecureRandom()"]
    Q["Internal call: arithmetic.encode()/decode()"]
    R["Internal call: hash.digest()"]
    S["Internal call: System.arraycopy()"]
    T["Internal call: new Sha256MAC()"]
    U["Internal call: mac.digest()"]
    V["Internal call: arithmetic.mul()"]
    W["Internal call: arithmetic.getGenerator()"]
    X["Internal call: arithmetic.isInGroup()"]
    Y["Internal call: new HauckTarget()"]

    A --> B
    A --> C
    A --> D
    A --> E
    A --> F
    F --> M
    F --> N
    A --> G
    G --> O
    G --> P
    A --> H
    H --> Q
    H --> R
    A --> I
    I --> Q
    I --> S
    I --> T
    A --> J
    J --> Q
    J --> U
    A --> K
    A --> L
    L --> G
    L --> V
    L --> W
    L --> H
    L --> X
    L --> Y
```

This code implements oblivious transfer functionality based on the Hauck protocol, primarily including core features such as key generation, hash computation, MAC initialization, and group element operations. The flowchart illustrates the class structure, attribute relationships, and method call chains, particularly highlighting how the generateHauckTarget() method iteratively generates qualified cryptographic target objects through critical steps like random number generation, elliptic curve point multiplication, and hash conversion. The methods collaborate via arithmetic operation components and hash components to ensure protocol security and correctness.

### Field List

| Name  | Type  | Description |
|-------|-------|------|
| hash | HashFunction | Declaration of hash function object. |
| arithmetic | GroupArithmetic | Common group arithmetic operations object arithmetic. |
| mac | HashBasedMessageAuthenticationCode | Hash Message Authentication Code Object |
| uuid | String | The public string variable uuid is used to store a unique identifier. |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| generateHauckTarget | HauckTarget | This method generates a HauckTarget object, iteratively produces a random number y, calculates s and t, and returns a new object containing y, s, t upon verifying that s is in the group and t.x is not -1. |
| hashTecElement | GroupElement | The method hashes the group element: first encodes it into a byte array, then computes the hash digest, and finally decodes it back into a group element for return. |
| getGroupElement | GroupElement | This method takes an object as input. If it is a string, it splits the string by commas, then creates and returns a point element on a Twisted Edwards curve using the two resulting values. |
| initMac | void | Initialize the MAC method by encoding s and r, then concatenating them as the key, and use Sha256MAC to generate the message authentication code. |
| macTecElement | byte[] | This method encodes the input GroupElement, generates a byte array, computes its MAC digest, and returns it. |
| genRandomScalar | BigInteger | Generate a random large integer within the range from 0 to a given large integer q, using a secure random number generator. |




