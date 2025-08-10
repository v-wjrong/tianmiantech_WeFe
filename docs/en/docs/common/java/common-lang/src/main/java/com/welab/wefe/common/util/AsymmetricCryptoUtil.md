# Basic Information

|      |      |
|------|------|
| Name | AsymmetricCryptoUtil |
| Language | .java |
| Code Path | WeFe/common/java/common-lang/src/main/java/com/welab/wefe/common/util/AsymmetricCryptoUtil.java |
| Package Name | com.welab.wefe.common.util |
| Dependencies | ['com.welab.wefe.common.constant.SecretKeyType'] |
| Brief Description | Asymmetric encryption utility class, supports public key encryption and private key decryption, defaults to RSA, with optional SM2. |

# Description

The AsymmetricCryptoUtil class provides asymmetric encryption functionality, containing two static methods. The encryptByPublicKey method encrypts plaintext using a public key, supporting both SM2 and RSA algorithms with RSA as the default. The decryptByPrivateKey method decrypts ciphertext using a private key, also supporting SM2 and RSA algorithms with RSA as the default. Both methods accept key strings and key type parameters, automatically selecting RSA when no type is specified.

# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| AsymmetricCryptoUtil | class | Asymmetric encryption utility class, supports public key encryption and private key decryption, defaults to RSA algorithm, with optional SM2. |



## Class AsymmetricCryptoUtil

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | AsymmetricCryptoUtil |
| Description | Asymmetric encryption utility class, supports public key encryption and private key decryption, defaults to RSA algorithm, with optional SM2. |


### UML Class Diagram

```mermaid
classDiagram
    class AsymmetricCryptoUtil {
        +encryptByPublicKey(String plaintext, String publicKeyStr, SecretKeyType secretKeyType) String
        +decryptByPrivateKey(String ciphertext, String privateKeyStr, SecretKeyType secretKeyType) String
    }

    class SecretKeyType {
        <<Enumeration>>
        rsa
        sm2
    }

    class SM2Util {
        +encryptByPublicKey(String plaintext, String publicKeyStr) String
        +decryptByPrivateKey(String ciphertext, String privateKeyStr) String
    }

    class RSAUtil {
        +encryptByPublicKey(String plaintext, String publicKeyStr) String
        +decryptByPrivateKey(String ciphertext, String privateKeyStr) String
    }

    AsymmetricCryptoUtil --> SecretKeyType : uses
    AsymmetricCryptoUtil --> SM2Util : invokes
    AsymmetricCryptoUtil --> RSAUtil : invokes
```

This diagram illustrates the structure of the asymmetric encryption utility class AsymmetricCryptoUtil, which selects encryption algorithms via the SecretKeyType enumeration and delegates specific operations to either SM2Util or RSAUtil. Core functionalities include public key encryption and private key decryption, supporting both RSA and SM2 algorithms with RSA as the default. The inter-class relationships clearly demonstrate the application of the strategy pattern.


### Internal Method Call Graph

```mermaid
graph TD
    A["Class AsymmetricCryptoUtil"]
    B["Method: encryptByPublicKey"]
    C["Parameters: plaintext, publicKeyStr, secretKeyType"]
    D["Default handling: secretKeyType = rsa"]
    E["switch secretKeyType"]
    F["case sm2: SM2Util.encryptByPublicKey"]
    G["default: RSAUtil.encryptByPublicKey"]
    H["Method: decryptByPrivateKey"]
    I["Parameters: ciphertext, privateKeyStr, secretKeyType"]
    J["Default handling: secretKeyType = rsa"]
    K["switch secretKeyType"]
    L["case sm2: SM2Util.decryptByPrivateKey"]
    M["default: RSAUtil.decryptByPrivateKey"]

    A --> B
    B --> C
    B --> D
    D --> E
    E -->|sm2| F
    E -->|default| G
    A --> H
    H --> I
    H --> J
    J --> K
    K -->|sm2| L
    K -->|default| M
```

This code demonstrates an asymmetric cryptographic utility class containing two core methods: public key encryption and private key decryption. The flowchart clearly presents the method invocation paths: first handling default values for key types, then routing to corresponding cryptographic implementations (SM2Util or RSAUtil) based on the key type (sm2/rsa). Both methods feature symmetrical structures including parameter validation, default value handling, and algorithm routing logic, reflecting excellent code reusability and extensibility design.

### Field List

| Name  | Type  | Description |
|-------|-------|------|

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| encryptByPublicKey | String | Encrypt plaintext using public key, supports RSA and SM2 algorithms, with RSA as default. |
| decryptByPrivateKey | String | This method decrypts text using a private key, supporting both RSA and SM2 algorithms, with RSA as the default. It invokes the corresponding decryption utility class based on the type of key provided. |




