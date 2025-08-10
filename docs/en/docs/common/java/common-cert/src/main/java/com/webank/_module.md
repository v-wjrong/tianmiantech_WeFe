# Basic Information

|      |      |
|------|------|
| Name | webank |
| Language | .java |
| Code Path | WeFe/common/java/common-cert/src/main/java/com/webank |
| Package Name | docs.common.java.common-cert.src.main.java.com.webank |
| Brief Description | Cryptography toolkit, including key management, certificate operations, and file handling. Supports RSA/ECDSA/SM2 algorithms, PFX/JKS parsing, and relies on BouncyCastle. Suitable for full-cycle PKI management, such as key generation, certificate issuance, and storage. Includes static utility classes like KeyUtils and CertUtils. |

# Description

## Overview  
This module is a cryptographic security toolkit, with core responsibilities including key pair management, certificate lifecycle operations, and basic file handling, resembling a lightweight PKI system implementation. The interface specifications cover key generation (supporting RSA/ECDSA/SM2 algorithms), certificate parsing (PFX/JKS formats), format conversion (PEM/PKCS#8), and X.500 attribute encapsulation. Key data structures include SM2 elliptic curve parameters, PKCS#8 private key format, CryptoKeyPair objects, and X.500 name models. External dependencies primarily include the BouncyCastle security library and Lombok utility. For example, KeyUtils implements SM2 key generation, CertService handles root certificate issuance, and X500NameInfo encapsulates DN attributes.  

## Key Business Scenarios  
The module is suitable for end-to-end digital certificate management, with typical scenarios including: 1) Key pair generation → certificate issuance → storage (e.g., SSL certificate deployment); 2) Certificate status tracking (WAIT_VERIFY → VALID); 3) CRL revocation list management. The interaction model employs static factory methods (e.g., ECKeyHandler.generateECKeyPair()) and the builder pattern (e.g., X509CertHandler chained calls). A typical application is in the national cryptographic scenario: SM2 key generation → SM3WITHSM2 signing → PEM format storage. API types encompass cryptographic operations (ECDSA verification), enum queries (KeyAlgorithmEnums), and IO operations (atomic file writing).


### Package Internal Structure View

```mermaid
graph TD
    webank --> cert
    cert --> toolkit
    toolkit --> utils
    toolkit --> constants
    toolkit --> enums
    toolkit --> encrypt
    toolkit --> service
    toolkit --> handler
    toolkit --> model
    utils --> KeyUtils.java
    utils --> FileOperationUtils.java
    utils --> CertUtils.java
    constants --> CertConstants.java
    enums --> CertStatusEnums.java
    enums --> KeyAlgorithmEnums.java
    enums --> CertDigestAlgEnums.java
    enums --> EccTypeEnums.java
    encrypt --> KeyPresenter.java
    encrypt --> PemEncrypt.java
    service --> CertService.java
    handler --> ECKeyHandler.java
    handler --> SM2KeyHandler.java
    handler --> X509CertHandler.java
    model --> X500NameInfo.java
```

This flowchart illustrates the Java package structure of the common-cert module in the WeFe project. Starting from com.webank.cert, it hierarchically expands to the toolkit utility package and its submodules, including utils utility classes, constants definitions, enums enumeration classes, encrypt encryption module, service service classes, handler processors, and model model classes, ultimately detailing each specific Java file.

# File List

| Name   | Type  | Description |
|-------|------|-------------|
| [cert](cert/_module.md) | package | Cryptography toolkit, including key management, certificate operations, and file handling. Supports RSA/ECDSA/SM2 algorithms, PFX/JKS parsing, and relies on BouncyCastle. Suitable for full-cycle PKI management, such as key generation, certificate issuance, and storage. Includes static utility classes like KeyUtils and CertUtils. |


