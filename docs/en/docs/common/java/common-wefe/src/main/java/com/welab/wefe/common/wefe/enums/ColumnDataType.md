# Basic Information

|      |      |
|------|------|
| Name | ColumnDataType |
| Language | .java |
| Code Path | WeFe/common/java/common-wefe/src/main/java/com/welab/wefe/common/wefe/enums/ColumnDataType.java |
| Package Name | com.welab.wefe.common.wefe.enums |
| Dependencies | [] |
| Brief Description | The enumeration type ColumnDataType defines seven data types: Integer, Long, Double, Boolean, Enum, String, and DateTime. |

# Description

This enumeration defines the types of column data, including seven categories: Integer represents whole numbers, Long represents long integers, Double represents double-precision floating-point numbers, Boolean represents boolean values, Enum represents enumerated types, String represents text strings, and DateTime represents date and time. Each type is accompanied by a comment explaining its meaning.

# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| ColumnDataType | enum | Define an enumeration for column data types, including integer, long integer, double precision, boolean, enumeration, string, and datetime. |



## Class ColumnDataType

|      |      |
|------|------|
| Access Modifier | public |
| Type | enum |
| Name | ColumnDataType |
| Description | Define an enumeration for column data types, including integer, long integer, double precision, boolean, enumeration, string, and datetime. |


### UML Class Diagram

```mermaid
classDiagram
    class ColumnDataType {
        <<enumeration>>
        +Integer
        +Long
        +Double
        +Boolean
        +Enum
        +String
        +DateTime
    }
```

This code defines an enumeration type named ColumnDataType, which represents different column data types. The enumeration includes 7 constant values: Integer (integer), Long (long integer), Double (double-precision floating-point), Boolean (boolean), Enum (enumeration), String (string), and DateTime (date and time). Such enumerations are typically used in database column type definitions or data format specification scenarios, ensuring type safety and consistency through predefined type sets. Each enumeration value corresponds to a specific data type, facilitating clear distinction and handling of different data formats in programs.


### Internal Method Call Graph

```mermaid
graph TD
    A["Enum Class ColumnDataType"]
    B["Enum Value: Integer"]
    C["Enum Value: Long"]
    D["Enum Value: Double"]
    E["Enum Value: Boolean"]
    F["Enum Value: Enum"]
    G["Enum Value: String"]
    H["Enum Value: DateTime"]

    A --> B
    A --> C
    A --> D
    A --> E
    A --> F
    A --> G
    A --> H
```

This flowchart illustrates the structure of the ColumnDataType enum class, which includes seven predefined data type enum values: Integer, Long, Double, Boolean, Enum, String, and DateTime. Each enum value is connected to the main class via arrows, indicating their membership in ColumnDataType. Such enum types are commonly used to define data type constraints for table columns or database fields, providing standardized type identifiers for the system.

### Field List

| Name  | Type  | Description |
|-------|-------|------|

### Method List

| Name  | Type  | Description |
|-------|-------|------|




