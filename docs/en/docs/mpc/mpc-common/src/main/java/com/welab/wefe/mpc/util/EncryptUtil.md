# Basic Information

|      |      |
|------|------|
| Name | EncryptUtil |
| Language | .java |
| Code Path | WeFe/mpc/mpc-common/src/main/java/com/welab/wefe/mpc/util/EncryptUtil.java |
| Package Name | com.welab.wefe.mpc.util |
| Dependencies | ['java.nio.charset.Charset', 'com.welab.wefe.mpc.commom.AccountEncryptionType', 'com.welab.wefe.mpc.commom.Conversion', 'com.welab.wefe.mpc.pir.protocol.se.SymmetricKey', 'com.welab.wefe.mpc.pir.protocol.se.aes.AESDecryptKey'] |
| Brief Description | The EncryptUtil class provides encryption and decryption functionalities, supporting MD5, SHA256, and SHA512 encryption methods, as well as AES-based decryption operations. |

# Description

The `EncryptUtil` class provides two encryption-related functionalities. The `encrypt` method performs hashing on a string based on the specified encryption type, supporting three algorithms: MD5, SHA256, and SHA512, with the original string returned by default. The `decryptByAES` method is used for AES decryption, accepting the encrypted result and a key. It first splits the encrypted data and the initialization vector, then decrypts using `AESDecryptKey`, and finally returns a UTF-8 formatted string.

# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| EncryptUtil | class | The EncryptUtil class provides encryption and decryption functionalities, supporting MD5, SHA256, and SHA512 encryption methods, as well as AES-based decryption methods, which require passing a key and an initialization vector. |



## Class EncryptUtil

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | EncryptUtil |
| Description | The EncryptUtil class provides encryption and decryption functionalities, supporting MD5, SHA256, and SHA512 encryption methods, as well as AES-based decryption methods, which require passing a key and an initialization vector. |


### UML Class Diagram

```mermaid
classDiagram
    class EncryptUtil {
        +encrypt(String id, String method) String
        +decryptByAES(String enResults, byte[] key) String
    }

    class AccountEncryptionType {
        <<Enumeration>>
        md5
        sha256
        sha512
    }

    class SHAUtil {
        <<Utility>>
        +SHAMD5(String input) String
        +SHA256(String input) String
        +SHA512(String input) String
    }

    class Conversion {
        <<Utility>>
        +hexStringToBytes(String hex) byte[]
    }

    class AESDecryptKey {
        -byte[] key
        -byte[] iv
        +AESDecryptKey(byte[] key, byte[] iv)
        +encrypt(byte[] input) byte[]
    }

    EncryptUtil --> AccountEncryptionType : uses
    EncryptUtil --> SHAUtil : calls
    EncryptUtil --> Conversion : calls
    EncryptUtil --> AESDecryptKey : creates instance
```

This class diagram illustrates the core structure and relationships of the encryption utility class `EncryptUtil`. The `EncryptUtil` provides two public methods: `encrypt()` and `decryptByAES()`, which rely on the enumeration type `AccountEncryptionType` for algorithm selection, invoke static methods of `SHAUtil` for hash computation, and utilize the `Conversion` utility class for byte conversion. The decryption functionality is achieved by creating an instance of `AESDecryptKey`, which encapsulates AES keys and initialization vectors. All utility classes are marked with `<<Utility>>`, reflecting the stateless design characteristic of utility classes.


### Internal Method Call Graph

```mermaid
graph TD
    A["Class EncryptUtil"]
    B["Static method: encrypt(String id, String method)"]
    C["Get encryption type: AccountEncryptionType.valueOf(method)"]
    D["Switch encryption type"]
    E["case md5: Call SHAUtil.SHAMD5(id)"]
    F["case sha256: Call SHAUtil.SHA256(id)"]
    G["case sha512: Call SHAUtil.SHA512(id)"]
    H["default: Return original id"]
    I["Static method: decryptByAES(String enResults, byte[] key)"]
    J["Split ciphertext: enResults.split','"]
    K["Convert ciphertext: Conversion.hexStringToBytes(realResult[0])"]
    L["Convert IV vector: Conversion.hexStringToBytes(realResult[1])"]
    M["Create AES key: new AESDecryptKey(key, iv)"]
    N["Decrypt operation: aesKey.encrypt(enResult)"]
    O["Return UTF-8 string: new String(result, Charset.forName'utf-8'"]

    A --> B
    B --> C
    C --> D
    D --> E
    D --> F
    D --> G
    D --> H
    A --> I
    I --> J
    J --> K
    J --> L
    K --> M
    L --> M
    M --> N
    N --> O
```

Flowchart description: This flowchart illustrates two core methods of the EncryptUtil class. The encrypt method invokes corresponding SHAUtil hash functions based on the input encryption type (md5/sha256/sha512), returning the original string by default. The decryptByAES method performs AES decryption: splitting ciphertext and IV vector, converting them to byte arrays, creating a decryption key object, and ultimately decrypting to return a UTF-8 string. The entire process clearly demonstrates the dispatch logic of encryption types and the data conversion steps in the decryption process.

### Field List

| Name  | Type  | Description |
|-------|-------|------|

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| encrypt | String | The static method `encrypt` selects the encryption type (MD5, SHA256, SHA512) based on the `method` parameter to encrypt the `id`. If no match is found, it returns the original `id`. |
| decryptByAES | String | This method decrypts a string using AES, taking an encrypted string and a key as input, and outputs the decrypted UTF-8 string. The process involves splitting the input, converting byte arrays, initializing the AES key, and performing decryption. |




