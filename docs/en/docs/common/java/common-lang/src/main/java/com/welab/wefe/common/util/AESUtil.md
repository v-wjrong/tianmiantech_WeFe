# Basic Information

|      |      |
|------|------|
| Name | AESUtil |
| Language | .java |
| Code Path | WeFe/common/java/common-lang/src/main/java/com/welab/wefe/common/util/AESUtil.java |
| Package Name | com.welab.wefe.common.util |
| Dependencies | ['com.welab.wefe.common.constant.Constant', 'org.apache.commons.codec.binary.Base64', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'javax.crypto.Cipher', 'javax.crypto.KeyGenerator', 'javax.crypto.spec.IvParameterSpec', 'javax.crypto.spec.SecretKeySpec', 'java.io.IOException', 'java.io.UnsupportedEncodingException', 'java.security.Key', 'java.security.SecureRandom'] |
| Brief Description | The AESUtil class provides AES encryption and decryption functionality, supporting ECB and CBC modes, and includes various encryption methods and exception handling. |

# Description

AESUtil is a utility class that provides AES encryption and decryption functionalities, supporting multiple encryption modes and padding schemes. The class defines two encryption types, AES/ECB/PKCS5Padding and AES/CBC/NoPadding, as well as a custom type AES2. Its main features include encryption and decryption operations for byte arrays and strings, supporting calls with different encryption types. The encryption method uses a key generator to produce keys and implements encryption/decryption through the Cipher class. The decryption method converts encrypted hexadecimal strings back to the original data. The class also offers an encryption method with an initial vector (IV) parameter to ensure data block alignment before encryption. Error handling is implemented by logging error messages. All methods are static and can be called directly.

# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| AESUtil | class | The AESUtil class provides AES encryption and decryption functionality, supporting ECB and CBC modes. It includes methods for encrypting and decrypting strings and byte arrays, handling different encryption types and exception logging. |



## Class AESUtil

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | AESUtil |
| Description | The AESUtil class provides AES encryption and decryption functionality, supporting ECB and CBC modes. It includes methods for encrypting and decrypting strings and byte arrays, handling different encryption types and exception logging. |


### UML Class Diagram

```mermaid
classDiagram
    class AESUtil {
        -LOG : Logger
        -AESTYPE : String = "AES/ECB/PKCS5Padding"
        -AES_CBC_NO_PADDING : String = "AES/CBC/NoPadding"
        +AES2 : String = "AES2"
        +encrypt(byte[] content, byte[] key) byte[]
        +encrypt(byte[] content, byte[] key, String type) byte[]
        +encrypt(String content, String key) String
        +encrypt(String content, String key, String type) String
        +decrypt(byte[] content, byte[] key) byte[]
        +decrypt(byte[] content, byte[] key, String type) byte[]
        +decrypt(String content, String key) String
        +decrypt(String content, String key, String type) String
        -aesSecure(byte[] content, byte[] key, int mode) byte[]
        +aesSecure2(byte[] encryptData, byte[] keyStr, int mode) byte[]
        +aesSecureWithViParam(String data, String key, String iv) String
        -generateKey(byte[] key) Key
    }

    class Cipher {
        <<Interface>>
        +ENCRYPT_MODE : int
        +DECRYPT_MODE : int
        +getInstance(String transformation) Cipher
        +init(int opmode, Key key) void
        +doFinal(byte[] input) byte[]
        +getBlockSize() int
    }

    class SecretKeySpec {
        <<Interface>>
        +SecretKeySpec(byte[] key, String algorithm)
    }

    class IvParameterSpec {
        <<Interface>>
        +IvParameterSpec(byte[] iv)
    }

    class KeyGenerator {
        <<Interface>>
        +getInstance(String algorithm) KeyGenerator
        +init(int keysize, SecureRandom random) void
        +generateKey() SecretKey
    }

    class SecureRandom {
        <<Interface>>
        +getInstance(String algorithm) SecureRandom
        +setSeed(byte[] seed) void
    }

    class Base64 {
        <<Interface>>
        +encodeToString(byte[] input) String
    }

    AESUtil --> Cipher : Uses
    AESUtil --> SecretKeySpec : Uses
    AESUtil --> IvParameterSpec : Uses
    AESUtil --> KeyGenerator : Uses
    AESUtil --> SecureRandom : Uses
    AESUtil --> Base64 : Uses
```

This code demonstrates an AES encryption utility class AESUtil, which provides multiple methods for AES encryption and decryption, supporting different encryption modes and padding schemes. The class includes static constants defining encryption algorithm types, along with overloaded encrypt and decrypt methods handling both byte array and string inputs/outputs. Private methods aesSecure and aesSecure2 implement the core encryption logic, while the aesSecureWithViParam method supports encryption with initialization vectors. The class relies on interfaces from the Java Cryptography Standard such as Cipher and SecretKeySpec, combining these interfaces to achieve AES encryption/decryption functionality, while utilizing Base64 for encoding conversion. The overall design reflects flexible support for various AES encryption scenarios, with enhanced robustness through exception handling and logging.


### Internal Method Call Graph

```mermaid
graph TD
    A["Class AESUtil"]
    B["Constants: LOG, AESTYPE, AES_CBC_NO_PADDING, AES2"]
    C["Method: byte[] encrypt(byte[], byte[])"]
    D["Method: byte[] encrypt(byte[], byte[], String)"]
    E["Method: String encrypt(String, String)"]
    F["Method: String encrypt(String, String, String)"]
    G["Method: byte[] decrypt(byte[], byte[])"]
    H["Method: byte[] decrypt(byte[], byte[], String)"]
    I["Method: String decrypt(String, String)"]
    J["Method: String decrypt(String, String, String)"]
    K["Method: byte[] aesSecure(byte[], byte[], int)"]
    L["Method: byte[] aesSecure2(byte[], byte[], int)"]
    M["Method: String aesSecureWithViParam(String, String, String)"]
    N["Method: Key generateKey(byte[])"]

    A --> B
    A --> C
    A --> D
    A --> E
    A --> F
    A --> G
    A --> H
    A --> I
    A --> J
    A --> K
    A --> L
    A --> M
    A --> N

    C --> K
    D --> L
    D --> K
    E --> C
    F --> D
    G --> K
    H --> L
    H --> K
    I --> G
    J --> H
    L --> N
    M -->|uses| B
```

This code demonstrates an AES encryption utility class AESUtil, which provides various methods for AES encryption and decryption. The class includes two encryption modes (AES/ECB/PKCS5Padding and AES/CBC/NoPadding) with corresponding encryption/decryption methods, supporting both byte array and string input/output. The core methods aesSecure and aesSecure2 implement the actual encryption/decryption logic, while other methods mainly serve as overloads and wrappers for different parameter types. The class also contains an encryption method with initialization vector (IV) - aesSecureWithViParam, and a key generation method generateKey. All methods handle potential exceptions and log errors.

### Field List

| Name  | Type  | Description |
|-------|-------|------|
| LOG = LoggerFactory.getLogger(AESUtil.class) | Logger | The AESUtil class defines a static immutable log object LOG. |
| AES_CBC_NO_PADDING = "AES/CBC/NoPadding" | String | AES encryption algorithm, CBC mode, no padding. |
| AESTYPE = "AES/ECB/PKCS5Padding" | String | AES encryption algorithm, ECB mode, PKCS5 padding. |
| AES2 = "AES2" | String | Defined a public static constant string AES2 with the value "AES2". |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| decrypt | String | The static method `decrypt` is used to decrypt string content. It takes encrypted content and a key as input, and returns the decrypted string. If an encoding exception occurs, it logs the error and returns null. |
| aesSecure | byte[] | Using the AES algorithm to encrypt or decrypt content, supporting encryption or decryption modes, generating secure random numbers based on keys, and logging exceptions. |
| encrypt | byte[] | The static method `encrypt` takes a byte array `content` and `key`, and returns the encrypted byte array using AES encryption mode. |
| decrypt | String | The static method `decrypt` is used to decrypt string content. It accepts content, a key, and a type parameter, and returns the decrypted string. If an encoding exception occurs, it logs the error and returns null. |
| encrypt | String | The static method `encrypt` is used to encrypt a string, accepting parameters for content, key, and type, and returns a hexadecimal string or null. Error logs are recorded in case of exceptions. |
| aesSecureWithViParam | String | This method uses AES CBC mode without padding to encrypt data, processes the input data length to align with the block size, encrypts it with a key and IV, and returns the Base64-encoded result. Returns null if an error occurs. |
| generateKey | Key | The method `generateKey` takes a byte array `key` and generates an AES key. On success, it returns a `SecretKeySpec`; on failure, it logs an error and returns `null`. |
| aesSecure2 | byte[] | The Java method `aesSecure2` uses the AES algorithm to encrypt and decrypt data. It accepts a byte array parameter and a mode, then returns the processed result. If an exception occurs, it logs the error. |
| encrypt | String | The static method `encrypt` takes a content string and a key string, converts them into byte arrays using UTF-8 encoding for encryption, and returns a hexadecimal string. If an exception occurs, it logs the error and returns `null`. |
| decrypt | byte[] | This is a Java static method for AES decryption. It takes encrypted content and a key as input, and returns the decrypted byte array. Internally, it calls the aesSecure method with the operation mode set to decryption. |
| decrypt | byte[] | The static method `decrypt` uses AES to decrypt the content `content` based on the type `type`, supporting two AES modes. |
| encrypt | byte[] | Encryption Method: Based on the type parameter, select the AES encryption method. For AES2 type, call aesSecure2; otherwise, call aesSecure, both using encryption mode. |




