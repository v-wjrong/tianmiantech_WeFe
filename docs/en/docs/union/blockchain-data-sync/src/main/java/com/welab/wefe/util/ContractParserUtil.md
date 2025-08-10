# Basic Information

|      |      |
|------|------|
| Name | ContractParserUtil |
| Language | .java |
| Code Path | WeFe/union/blockchain-data-sync/src/main/java/com/welab/wefe/util/ContractParserUtil.java |
| Package Name | com.welab.wefe.util |
| Dependencies | ['com.welab.wefe.bo.contract.ContractContextInfo', 'com.welab.wefe.bo.contract.ContractInfo', 'com.welab.wefe.common.util.StringUtil', 'org.apache.commons.collections4.CollectionUtils', 'java.util.HashMap', 'java.util.List', 'java.util.Map'] |
| Brief Description | The ContractParserUtil class parses the contract information list, filters out invalid data, maps the binary and contract name to the ContractInfo object respectively, and stores it in the global context. |

# Description

The `ContractParserUtil` class contains a static method `parse` designed to process a list of `ContractInfo` objects. The method first checks if the list is empty and returns immediately if so. It then creates two HashMaps to store `ContractInfo` objects, using binary code and contract names as keys respectively. During iteration, entries with empty ABI or binary fields are skipped, while valid data is stored in the corresponding Map. Finally, the contents of the two temporary Maps are merged into the static Maps of the `ContractContextInfo` class. This entire process achieves categorized storage of contract information.

# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| ContractParserUtil | class | The `ContractParserUtil` class provides a static method `parse` that processes a list of contract information, filters out invalid data, maps the contract binary and name to the respective contract information, and stores it in the global context. |



## Class ContractParserUtil

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | ContractParserUtil |
| Description | The `ContractParserUtil` class provides a static method `parse` that processes a list of contract information, filters out invalid data, maps the contract binary and name to the respective contract information, and stores it in the global context. |


### UML Class Diagram

```mermaid
classDiagram
    class ContractParserUtil {
        +parse(List~ContractInfo~ contractInfoList) void
    }

    class ContractInfo {
        <<Interface>>
        +String getAbi()
        +String getBinary()
        +String getContractName()
    }

    class ContractContextInfo {
        <<static>>
        +Map~String, ContractInfo~ CONTRACT_BINARY_MAP
        +Map~String, ContractInfo~ CONTRACT_INFO_MAP
    }

    class StringUtil {
        <<static>>
        +isEmpty(String str) boolean
    }

    class CollectionUtils {
        <<static>>
        +isEmpty(Collection~?~ coll) boolean
    }

    ContractParserUtil --> CollectionUtils : Dependency
    ContractParserUtil --> StringUtil : Dependency
    ContractParserUtil --> ContractInfo : Dependency
    ContractParserUtil --> ContractContextInfo : Dependency
```

This code demonstrates a contract parsing utility class `ContractParserUtil`, which processes a list of contract information through its static method `parse`. Its primary function is to filter invalid contract data and store valid data into two static mapping tables. The class diagram clearly illustrates the dependency relationships between the utility class and utility libraries (`CollectionUtils`/`StringUtil`), the contract information interface (`ContractInfo`), and the context storage class (`ContractContextInfo`), reflecting the complete workflow of data validation, filtering, and storage.


### Internal Method Call Graph

```mermaid
graph TD
    A["parse(List<ContractInfo> contractInfoList)"]
    B["Check collection null: CollectionUtils.isEmpty(contractInfoList)"]
    C["Create Map: contractBinaryMap/HashMap"]
    D["Create Map: contractInfoMap/HashMap"]
    E["Iterate contractInfoList"]
    F["Get abi/binary: contractInfo.getAbi()/getBinary()"]
    G["Check null: StringUtil.isEmpty(abi/binary)"]
    H["Store in contractBinaryMap: put(binary, contractInfo)"]
    I["Store in contractInfoMap: put(contractName, contractInfo)"]
    J["Update global Map: CONTRACT_BINARY_MAP.putAll()"]
    K["Update global Map: CONTRACT_INFO_MAP.putAll()"]

    A --> B
    B --"Empty collection"--> K["Return directly"]
    B --"Non-empty"--> C
    C --> D
    D --> E
    E --> F
    F --> G
    G --"Has null"--> E
    G --"No null"--> H
    H --> I
    I --> E
    E --"Iteration ends"--> J
    J --> K
```

This flowchart describes the complete logical flow of the `ContractParserUtil.parse()` method. The method first checks if the input collection is empty, returning directly if true; otherwise creates two temporary HashMaps for storing contract data. During iteration, contracts with null ABI or Binary are filtered out, while valid data is stored in corresponding Maps. Finally, the contents of temporary Maps are merged into the global static `ContractContextInfo` Map. Key steps include null checks, data filtering, and two-level Map merging.

### Field List

| Name  | Type  | Description |
|-------|-------|------|

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| parse | void | Parse the contract information list, filter out invalid data, then map the binary and contract name to the contract information respectively, and store it in the global context. |




