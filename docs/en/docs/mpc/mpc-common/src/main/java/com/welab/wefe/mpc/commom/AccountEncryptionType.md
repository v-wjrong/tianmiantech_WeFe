# Basic Information

|      |      |
|------|------|
| Name | AccountEncryptionType |
| Language | .java |
| Code Path | WeFe/mpc/mpc-common/src/main/java/com/welab/wefe/mpc/commom/AccountEncryptionType.java |
| Package Name | com.welab.wefe.mpc.commom |
| Dependencies | [] |
| Brief Description | Enumeration defines account encryption types: plaintext, md5, sha256, sha512. |

# Description

This enumeration defines the encryption types for account passwords, including four options: plaintext (plain), MD5 encryption (md5), SHA256 encryption (sha256), and SHA512 encryption (sha512). Each type has corresponding comments explaining its encryption method.

# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| AccountEncryptionType | enum | The enumeration AccountEncryptionType defines four account encryption types: plaintext, md5, sha256, and sha512. |



## Class AccountEncryptionType

|      |      |
|------|------|
| Access Modifier | public |
| Type | enum |
| Name | AccountEncryptionType |
| Description | The enumeration AccountEncryptionType defines four account encryption types: plaintext, md5, sha256, and sha512. |


### UML Class Diagram

```mermaid
classDiagram
    class AccountEncryptionType {
        <<enumeration>>
        +plain
        +md5
        +sha256
        +sha512
    }
```

This code defines an enumeration type named AccountEncryptionType, which represents different encryption methods for account passwords. The enumeration includes four values: plain indicates plaintext storage, md5 represents encryption using the MD5 algorithm, sha256 denotes encryption with the SHA-256 algorithm, and sha512 signifies encryption with the SHA-512 algorithm. Enumeration types are typically used to define a set of fixed constants. Here, the enumeration clearly limits the available encryption options, facilitating unified management and usage of these encryption methods in code while avoiding potential errors caused by magic strings.


### Internal Method Call Graph

```mermaid
graph TD
    A["Enum AccountEncryptionType"]
    B["Enum value: plain"]
    C["Enum value: md5"]
    D["Enum value: sha256"]
    E["Enum value: sha512"]
    F["Comment: 'Plaintext'"]
    G["Comment: 'MD5 encryption'"]
    H["Comment: 'SHA256 encryption'"]
    I["Comment: 'SHA512 encryption'"]

    A --> B
    A --> C
    A --> D
    A --> E
    B -.-> F
    C -.-> G
    D -.-> H
    E -.-> I
```

This flowchart illustrates the structure of the AccountEncryptionType enum, which includes four enum values (plain, md5, sha256, sha512) along with their corresponding comment descriptions. Each enum value is connected via dashed lines to its documentation comments, clearly presenting the semantic definitions of different encryption types. This design is commonly used in configuration systems to represent optional encryption algorithm types.

### Field List

| Name  | Type  | Description |
|-------|-------|------|

### Method List

| Name  | Type  | Description |
|-------|-------|------|




