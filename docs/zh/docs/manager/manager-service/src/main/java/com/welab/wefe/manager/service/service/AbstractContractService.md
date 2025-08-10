# 基础信息

|      |      |
|------|------|
| 名称 | AbstractContractService |
| 编码语言 | .java |
| 代码路径 | WeFe/manager/manager-service/src/main/java/com/welab/wefe/manager/service/service/AbstractContractService.java |
| 包名 | com.welab.wefe.manager.service.service |
| 依赖项 | ['com.alibaba.fastjson.JSONArray', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.JObject', 'org.fisco.bcos.sdk.transaction.model.dto.TransactionResponse'] |
| 概述说明 | AbstractContractService类提供多个方法检查区块链交易状态，包括成功、失败、数据存在与否等，通过解析JSON响应值判断结果，异常时抛出错误。 |

# 说明

AbstractContractService类提供了多个方法用于检查区块链交易执行结果。主要功能包括判断交易是否成功、处理交易异常情况以及检测特定错误状态。transactionIsSuccess方法有两个重载版本，一个直接解析响应字符串，另一个处理TransactionResponse对象并针对不同错误码抛出异常。其他辅助方法可检测数据不存在、数据已存在和插入失败等特定情况。所有方法都通过解析JSON格式的响应值进行判断，确保交易状态检查的准确性和全面性。

# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| AbstractContractService | class | AbstractContractService类提供多个方法检查区块链交易状态，包括成功、异常、数据不存在、数据已存在及插入失败等情况，通过解析JSON响应值判断结果。 |



## 类 AbstractContractService

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | AbstractContractService |
| 说明 | AbstractContractService类提供多个方法检查区块链交易状态，包括成功、异常、数据不存在、数据已存在及插入失败等情况，通过解析JSON响应值判断结果。 |


### UML类图

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

    AbstractContractService --> TransactionResponse : 依赖
    AbstractContractService --> StatusCodeWithException : 依赖
    StatusCodeWithException --> StatusCode : 依赖
```

类图描述：
AbstractContractService是一个抽象类，提供了多个事务状态判断方法，主要处理区块链交易响应结果。它依赖TransactionResponse接口获取交易数据，并通过StatusCodeWithException处理异常情况。该类核心功能包括：判断交易是否成功、检测数据是否存在、处理插入失败等场景，所有方法都基于JSON格式的响应值进行解析，针对不同错误代码抛出特定异常或返回布尔结果。


### 内部方法调用关系图

```mermaid
graph TD
    A["类AbstractContractService"]
    B["方法: boolean transactionIsSuccess(String responseValues)"]
    C["方法: boolean transactionIsSuccess(TransactionResponse)"]
    D["方法: boolean transactionException(String)"]
    E["方法: boolean transactionDataNotFound(String)"]
    F["方法: boolean transactionDataIsExist(String)"]
    G["方法: boolean transactionInsertFail(String)"]

    A --> B
    A --> C
    A --> D
    A --> E
    A --> F
    A --> G

    B --> B1["解析JSONArray values"]
    B --> B2{"values为空或首元素<0?"}
    B2 -->|是| B3["返回false"]
    B2 -->|否| B4["返回true"]

    C --> C1["解析JSONArray values"]
    C --> C2{"values为空?"}
    C2 -->|是| C3["抛出SYSTEM_BUSY异常"]
    C2 -->|否| C4["获取retCode"]
    C4 --> C5{"retCode匹配?"}
    C5 -->|0| C6["返回true"]
    C5 -->|-1| C7["抛出'数据已存在'异常"]
    C5 -->|-2| C8["抛出'交易失败'异常"]
    C5 -->|-3| C9["抛出'数据不存在'异常"]
    C5 -->|其他| C10["抛出'未知响应码'异常"]

    D --> D1["解析JSONArray values"]
    D --> D2{"values为空?"}
    D2 -->|是| D3["返回true"]
    D2 -->|否| D4["返回false"]

    E --> E1["调用transactionException"]
    E --> E2{"非异常且retCode=-3?"}
    E2 -->|是| E3["返回true"]
    E2 -->|否| E4["返回false"]

    F --> F1["调用transactionException"]
    F --> F2{"非异常且retCode=-1?"}
    F2 -->|是| F3["返回true"]
    F2 -->|否| F4["返回false"]

    G --> G1["调用transactionException"]
    G --> G2{"非异常且retCode=-2?"}
    G2 -->|是| G3["返回true"]
    G2 -->|否| G4["返回false"]
```

该流程图描述了AbstractContractService类中多个交易状态判断方法的逻辑流程。核心方法transactionIsSuccess有两个重载版本，分别处理字符串响应和TransactionResponse对象，其他方法如transactionDataNotFound等均依赖transactionException进行基础校验。所有方法均通过解析JSON响应数据并检查特定状态码来实现不同场景的交易状态判断，包含正常成功、数据已存在、交易失败等情况的处理路径。异常处理流程会抛出带状态码的系统繁忙异常。

### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| transactionIsSuccess | boolean | 检查响应值是否为有效JSON数组且首元素非负，满足则返回成功，否则失败。 |
| transactionIsSuccess | boolean | 检查交易响应是否成功：解析JSON数组，返回码0为成功，非0抛出对应异常（数据已存在、交易失败、数据不存在或未知错误）。 |
| transactionDataNotFound | boolean | 检查响应数据是否未找到交易数据：非异常且首值为-3时返回真。 |
| transactionDataIsExist | boolean | 检查交易数据是否存在：解析JSON数组，确认无异常且首元素为-1。 |
| transactionException | boolean | 检查响应值是否为无效JSON数组，若为空或null则返回true。 |
| transactionInsertFail | boolean | 检查事务插入失败：解析JSON数组，非事务异常且首元素为-2时返回真。 |




