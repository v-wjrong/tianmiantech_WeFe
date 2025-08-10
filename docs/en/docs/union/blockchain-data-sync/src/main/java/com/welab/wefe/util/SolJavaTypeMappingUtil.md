# Basic Information

|      |      |
|------|------|
| Name | SolJavaTypeMappingUtil |
| Language | .java |
| Code Path | WeFe/union/blockchain-data-sync/src/main/java/com/welab/wefe/util/SolJavaTypeMappingUtil.java |
| Package Name | com.welab.wefe.util |
| Dependencies | ['org.apache.commons.lang3.StringUtils'] |
| Brief Description | The `SolJavaTypeMappingUtil` class maps Solidity primitive types to Java types: array types return `String`; `address`, `string`, and the `bytes` series return `String`; `bool` returns `Boolean`; integer types return `long`; other types default to returning `String`. |

# Description

The SolJavaTypeMappingUtil class contains a static method `fromSolBasicTypeToJavaType` that maps Solidity basic types to Java types. If the input type contains square brackets, it returns String. The address, string, and bytes series types are mapped to String, bool is mapped to Boolean, all uint and int series numeric types are mapped to long, and other cases default to returning String. This method implements the basic type conversion logic from Solidity to Java.

# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| SolJavaTypeMappingUtil | class | The SolJavaTypeMappingUtil class maps Solidity primitive types to Java types: array types, address, string, and byte types are mapped to String; boolean type is mapped to Boolean; integer types are mapped to long; other types default to String. |



## Class SolJavaTypeMappingUtil

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | SolJavaTypeMappingUtil |
| Description | The SolJavaTypeMappingUtil class maps Solidity primitive types to Java types: array types, address, string, and byte types are mapped to String; boolean type is mapped to Boolean; integer types are mapped to long; other types default to String. |


### UML Class Diagram

```mermaid
classDiagram
    class SolJavaTypeMappingUtil {
        +String fromSolBasicTypeToJavaType(String solBasicType)
    }
```

```mermaid
flowchart TD
    A["Start: fromSolBasicTypeToJavaType(solBasicType)"] --> B{"Does solBasicType contain '[' and ']'?"}
    B -- Yes --> C["Return 'String'"]
    B -- No --> D["Check solBasicType type"]
    D --> E{"Is address/string/bytes series?"}
    E -- Yes --> F["Return 'String'"]
    E -- No --> G{"Is bool?"}
    G -- Yes --> H["Return 'Boolean'"]
    G -- No --> I{"Is uint/int numeric series?"}
    I -- Yes --> J["Return 'long'"]
    I -- No --> K["Return 'String'"]
    C --> L["End"]
    F --> L
    H --> L
    J --> L
    K --> L
```

This code implements a utility class for mapping Solidity basic types to Java types. The class diagram shows it's a utility class containing only static methods, while the flowchart clearly illustrates its three-level decision logic: first checking for array types, then handling specific string types, and finally processing numeric types. The method maps Solidity's address, string, and bytes series to Java's String, bool to Boolean, all integer types to long, and defaults to returning String otherwise. This type conversion is particularly useful for interactions between blockchain smart contracts and Java applications.


### Internal Method Call Graph

```mermaid
graph TD
    A["Method: fromSolBasicTypeToJavaType(String solBasicType)"]
    B["Check if contains '[' and ']'"]
    C["Return 'String'"]
    D["switch(solBasicType)"]
    E["case 'address' to 'bytes32' etc."]
    F["Return 'String'"]
    G["case 'bool'"]
    H["Return 'Boolean'"]
    I["case 'uint8' to 'int256' etc."]
    J["Return 'long'"]
    K["default"]
    L["Return 'String'"]

    A --> B
    B -- Yes --> C
    B -- No --> D
    D --> E --> F
    D --> G --> H
    D --> I --> J
    D --> K --> L
```

This flowchart describes the execution logic of the `fromSolBasicTypeToJavaType` method in the `SolJavaTypeMappingUtil` class. The method first checks if the input string contains array symbols, and if so, directly returns "String". Otherwise, it maps Solidity basic types to Java types via a switch-case structure: address/bytes types return "String", boolean types return "Boolean", various integer types return "long", and the default case returns "String". The flowchart clearly illustrates the branching decision process of the type conversion.

### Field List

| Name  | Type  | Description |
|-------|-------|------|

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| fromSolBasicTypeToJavaType | String | This method converts Solidity basic types to Java types: array types return String; address, string, and bytes series return String; bool returns Boolean; integer types return long; others default to String. |




