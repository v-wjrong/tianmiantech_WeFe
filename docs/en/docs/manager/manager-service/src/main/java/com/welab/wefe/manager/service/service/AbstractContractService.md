# Basic Information

|      |      |
|------|------|
| Name | AbstractContractService |
| Language | .java |
| Code Path | WeFe/manager/manager-service/src/main/java/com/welab/wefe/manager/service/service/AbstractContractService.java |
| Package Name | com.welab.wefe.manager.service.service |
| Dependencies | ['com.alibaba.fastjson.JSONArray', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.JObject', 'org.fisco.bcos.sdk.transaction.model.dto.TransactionResponse'] |
| Brief Description | The `AbstractContractService` class provides multiple methods to check the status of blockchain transactions, including success, failure, and the presence or absence of data. It determines the result by parsing JSON response values and throws errors in case of exceptions. |

# Description

The `AbstractContractService` class provides multiple methods for checking blockchain transaction execution results. Its primary functionalities include determining whether a transaction succeeded, handling transaction exceptions, and detecting specific error states. The `transactionIsSuccess` method has two overloaded versions: one directly parses the response string, while the other processes a `TransactionResponse` object and throws exceptions for different error codes. Additional helper methods can detect specific scenarios such as non-existent data, pre-existing data, and insertion failures. All methods perform checks by parsing JSON-formatted response values, ensuring the accuracy and comprehensiveness of transaction status verification.

# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| AbstractContractService | class | The AbstractContractService class provides multiple methods to check the status of blockchain transactions, including success, exceptions, non-existent data, existing data, and insertion failures, by parsing JSON response values to determine the results. |



## Class AbstractContractService

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | AbstractContractService |
| Description | The AbstractContractService class provides multiple methods to check the status of blockchain transactions, including success, exceptions, non-existent data, existing data, and insertion failures, by parsing JSON response values to determine the results. |


### UML Class Diagram

```mermaid
classDiagram
    class AbstractContractService {
        <<Abstract>>
        +transactionIsSuccess(String responseValues) boolean
        +transactionIsSuccess(TransactionResponse transactionResponse) boolean
        +transactionException(String responseValues) boolean
        +transactionDataNotFound(String responseValues) boolean
        +transactionDataIsExist(String responseValues) boolean
        +transactionInsertFail(String responseValues) boolean
    }

    class TransactionResponse {
        <<Interface>>
        +getValues() String
        +getReturnMessage() String
    }

    class StatusCodeWithException {
        +StatusCodeWithException(StatusCode code, String message)
    }

    class StatusCode {
        <<Enumeration>>
        +SYSTEM_BUSY
    }

    AbstractContractService --> TransactionResponse : Dependency
    AbstractContractService --> StatusCodeWithException : Dependency
    StatusCodeWithException --> StatusCode : Dependency
```

Class Diagram Description:
AbstractContractService is an abstract class that provides multiple transaction state judgment methods, primarily handling blockchain transaction response results. It depends on the TransactionResponse interface to obtain transaction data and processes exceptions through StatusCodeWithException. The core functionalities of this class include: determining whether a transaction is successful, checking if data exists, handling insertion failure scenarios, etc. All methods parse JSON-formatted response values, throwing specific exceptions or returning boolean results based on different error codes.


### Internal Method Call Graph

```mermaid
graph TD
    A["Class AbstractContractService"]
    B["Method: boolean transactionIsSuccess(String responseValues)"]
    C["Method: boolean transactionIsSuccess(TransactionResponse)"]
    D["Method: boolean transactionException(String)"]
    E["Method: boolean transactionDataNotFound(String)"]
    F["Method: boolean transactionDataIsExist(String)"]
    G["Method: boolean transactionInsertFail(String)"]

    A --> B
    A --> C
    A --> D
    A --> E
    A --> F
    A --> G

    B --> B1["Parse JSONArray values"]
    B --> B2{"Is values empty or first element <0?"}
    B2 -->|Yes| B3["Return false"]
    B2 -->|No| B4["Return true"]

    C --> C1["Parse JSONArray values"]
    C --> C2{"Is values empty?"}
    C2 -->|Yes| C3["Throw SYSTEM_BUSY exception"]
    C2 -->|No| C4["Get retCode"]
    C4 --> C5{"Does retCode match?"}
    C5 -->|0| C6["Return true"]
    C5 -->|-1| C7["Throw 'Data already exists' exception"]
    C5 -->|-2| C8["Throw 'Transaction failed' exception"]
    C5 -->|-3| C9["Throw 'Data not found' exception"]
    C5 -->|Others| C10["Throw 'Unknown response code' exception"]

    D --> D1["Parse JSONArray values"]
    D --> D2{"Is values empty?"}
    D2 -->|Yes| D3["Return true"]
    D2 -->|No| D4["Return false"]

    E --> E1["Call transactionException"]
    E --> E2{"No exception and retCode=-3?"}
    E2 -->|Yes| E3["Return true"]
    E2 -->|No| E4["Return false"]

    F --> F1["Call transactionException"]
    F --> F2{"No exception and retCode=-1?"}
    F2 -->|Yes| F3["Return true"]
    F2 -->|No| F4["Return false"]

    G --> G1["Call transactionException"]
    G --> G2{"No exception and retCode=-2?"}
    G2 -->|Yes| G3["Return true"]
    G2 -->|No| G4["Return false"]
```

This flowchart illustrates the logical flows of multiple transaction status judgment methods in the AbstractContractService class. The core method transactionIsSuccess has two overloaded versions handling string responses and TransactionResponse objects respectively, while other methods like transactionDataNotFound rely on transactionException for basic validation. All methods parse JSON response data and check specific status codes to determine transaction states across scenarios, including normal success, data existence, transaction failure, etc. The exception handling flow throws system busy exceptions with status codes.

### Field List

| Name  | Type  | Description |
|-------|-------|------|

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| transactionIsSuccess | boolean | Check if the response value is a valid JSON array and its first element is non-negative. Return success if satisfied, otherwise return failure. |
| transactionIsSuccess | boolean | Check if the transaction response is successful: Parse the JSON array, where a return code of 0 indicates success, and non-zero codes throw corresponding exceptions (data already exists, transaction failed, data does not exist, or unknown error). |
| transactionDataNotFound | boolean | Check if the response data indicates no transaction data found: return true when non-exceptional and the first value is -3. |
| transactionDataIsExist | boolean | Check if transaction data exists: Parse the JSON array to confirm there are no exceptions and the first element is -1. |
| transactionException | boolean | Check if the response value is an invalid JSON array, and return true if it is empty or null. |
| transactionInsertFail | boolean | Check transaction insertion failure: Return true when parsing a JSON array, if it's a non-transactional exception and the first element is -2. |




