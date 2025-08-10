# 基础信息

|      |      |
|------|------|
| 名称 | NaorPinkasQuery |
| 编码语言 | .java |
| 代码路径 | WeFe/mpc/mpc-pir/mpc-pir-sdk/src/main/java/com/welab/wefe/mpc/pir/sdk/naor/NaorPinkasQuery.java |
| 包名 | com.welab.wefe.mpc.pir.sdk.naor |
| 依赖项 | ['java.math.BigInteger', 'java.util.UUID', 'org.apache.commons.lang3.StringUtils', 'com.welab.wefe.mpc.commom.Constants', 'com.welab.wefe.mpc.pir.protocol.ro.hf.HashFunction', 'com.welab.wefe.mpc.pir.protocol.ro.hf.Sha256', 'com.welab.wefe.mpc.pir.request.QueryKeysRequest', 'com.welab.wefe.mpc.pir.request.naor.QueryNaorPinkasRandomResponse', 'com.welab.wefe.mpc.pir.request.naor.QueryNaorPinkasResultRequest', 'com.welab.wefe.mpc.pir.request.naor.QueryNaorPinkasResultResponse', 'com.welab.wefe.mpc.pir.sdk.config.PrivateInformationRetrievalConfig', 'com.welab.wefe.mpc.pir.sdk.trasfer.NaorPinkasTransferVariable', 'com.welab.wefe.mpc.util.DiffieHellmanUtil', 'com.welab.wefe.mpc.util.EncryptUtil'] |
| 概述说明 | NaorPinkasQuery类实现私有信息检索，通过Diffie-Hellman密钥交换和AES加密安全获取目标索引数据。 |

# 说明

NaorPinkasQuery类实现了基于Naor-Pinkas不经意传输协议的私有信息检索查询功能。该类包含两个重载方法，核心方法接收配置参数、传输变量和密钥大小，默认密钥大小为1024位。方法首先生成随机密钥k，构建随机查询请求并获取响应，验证响应有效性后提取参数。通过Diffie-Hellman加密生成公钥pk，处理目标索引偏移量后发送结果请求。最后使用SHA-256哈希和AES解密返回目标索引的加密结果。整个过程实现了安全的信息检索，确保查询隐私性。

# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| NaorPinkasQuery | class | NaorPinkasQuery类实现私有信息检索功能，通过Diffie-Hellman密钥交换和AES加密确保数据安全，支持自定义密钥大小和异常处理。 |



## 类 NaorPinkasQuery

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | NaorPinkasQuery |
| 说明 | NaorPinkasQuery类实现私有信息检索功能，通过Diffie-Hellman密钥交换和AES加密确保数据安全，支持自定义密钥大小和异常处理。 |


### UML类图

```mermaid
classDiagram
    class NaorPinkasQuery {
        +query(PrivateInformationRetrievalConfig config, NaorPinkasTransferVariable transferVariable) String
        +query(PrivateInformationRetrievalConfig config, NaorPinkasTransferVariable transferVariable, int keySize) String
    }

    class PrivateInformationRetrievalConfig {
        +getTargetIndex() int
        +getPrimaryKeys() List~String~
        +getRequestId() String
    }

    class NaorPinkasTransferVariable {
        +queryNaorPinkasRandom(QueryKeysRequest request) QueryNaorPinkasRandomResponse
        +queryNaorPinkasResult(QueryNaorPinkasResultRequest request) QueryNaorPinkasResultResponse
    }

    class QueryKeysRequest {
        +setIds(List~String~ ids) void
        +setOtMethod(String method) void
        +setRequestId(String id) void
    }

    class QueryNaorPinkasRandomResponse {
        +getCode() int
        +getMessage() String
        +getUuid() String
        +getG() String
        +getP() String
        +getSecret() String
        +getRandoms() List~String~
    }

    class QueryNaorPinkasResultRequest {
        +setUuid(String uuid) void
        +setPk(String pk) void
    }

    class QueryNaorPinkasResultResponse {
        +getCode() int
        +getMessage() String
        +getEncryptResults() List~String~
    }

    class DiffieHellmanUtil {
        <<Utility>>
        +generateRandomKey(int keySize) BigInteger
        +hexStringToBigInteger(String hex) BigInteger
        +encrypt(BigInteger g, BigInteger k, BigInteger p) BigInteger
        +modDivide(BigInteger a, BigInteger b, BigInteger p) BigInteger
        +bigIntegerToHexString(BigInteger num) String
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

    NaorPinkasQuery --> PrivateInformationRetrievalConfig : 依赖
    NaorPinkasQuery --> NaorPinkasTransferVariable : 依赖
    NaorPinkasQuery --> DiffieHellmanUtil : 依赖
    NaorPinkasQuery --> EncryptUtil : 依赖
    NaorPinkasQuery --> HashFunction : 依赖
    NaorPinkasTransferVariable --> QueryKeysRequest : 依赖
    NaorPinkasTransferVariable --> QueryNaorPinkasRandomResponse : 依赖
    NaorPinkasTransferVariable --> QueryNaorPinkasResultRequest : 依赖
    NaorPinkasTransferVariable --> QueryNaorPinkasResultResponse : 依赖
    Sha256 ..|> HashFunction : 实现
```

类图描述：该图展示了NaorPinkasQuery类与多个辅助类的关系，包括配置类PrivateInformationRetrievalConfig、传输变量类NaorPinkasTransferVariable、请求响应类（QueryKeysRequest等）、加密工具类DiffieHellmanUtil和EncryptUtil，以及哈希接口HashFunction及其实现Sha256。NaorPinkasQuery通过组合这些类实现基于Naor-Pinkas不经意传输协议的隐私信息检索功能。


### 内部方法调用关系图

```mermaid
graph TD
    A["NaorPinkasQuery.query入口"]
    B["获取targetIndex和随机数k"]
    C["构建QueryKeysRequest"]
    D["设置requestId/OT方法/主键"]
    E["调用transferVariable.queryNaorPinkasRandom"]
    F{"randomResponse.code==0?"}
    G["抛出异常"]
    H["解析g/p/secret参数"]
    I["计算pk=g^k mod p"]
    J{"targetIndex!=0?"}
    K["调整pk值"]
    L["构建QueryNaorPinkasResultRequest"]
    M["调用transferVariable.queryNaorPinkasResult"]
    N{"response.code==0?"}
    O["抛出异常"]
    P["生成AES密钥"]
    Q["返回解密结果"]

    A --> B
    B --> C
    C --> D
    D --> E
    E --> F
    F -- 否 --> G
    F -- 是 --> H
    H --> I
    I --> J
    J -- 是 --> K
    K --> L
    J -- 否 --> L
    L --> M
    M --> N
    N -- 否 --> O
    N -- 是 --> P
    P --> Q
```

该流程图展示了NaorPinkas隐私信息检索协议的完整查询流程。从初始化参数开始，经过两轮OT协议交互（随机数获取和结果查询），包含异常处理、Diffie-Hellman密钥计算和AES解密等关键步骤，最终返回目标索引的解密结果。整个过程严格遵循Naor-Pinkas协议规范，确保在不暴露查询目标的情况下安全获取数据。

### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| query | String | 该方法执行Naor-Pinkas加密查询，生成随机密钥，处理请求和响应，进行Diffie-Hellman加密计算，最终解密并返回目标索引结果。 |
| query | String | Java方法：根据配置和传输变量查询信息，默认缓冲区大小1024，可能抛出异常。 |




