# 基础信息

|      |      |
|------|------|
| 名称 | TrustCertsContractEventParser |
| 编码语言 | .java |
| 代码路径 | WeFe/union/blockchain-data-sync/src/main/java/com/welab/wefe/parser/TrustCertsContractEventParser.java |
| 包名 | com.welab.wefe.parser |
| 依赖项 | ['com.alibaba.fastjson.JSONObject', 'com.welab.wefe.BlockchainDataSyncApp', 'com.welab.wefe.common.data.mongodb.entity.union.TrustCerts', 'com.welab.wefe.common.data.mongodb.entity.union.ext.TrustCertsExtJSON', 'com.welab.wefe.common.data.mongodb.repo.TrustCertsMongoRepo', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.constant.EventConstant', 'com.welab.wefe.exception.BusinessException', 'org.apache.commons.lang3.StringUtils'] |
| 概述说明 | 解析区块链信任证书事件的Java类，处理插入和删除操作，使用MongoDB存储数据。 |

# 说明

TrustCertsContractEventParser类继承AbstractParser，用于解析信任证书合约事件。它依赖TrustCertsMongoRepo进行数据库操作，包含两个主要方法：parseInsertEvent处理证书插入事件，设置证书各项属性并保存到MongoDB；parseDeleteBySerialNumberEvent根据序列号删除证书记录。主方法parseContractEvent通过事件名称路由到对应处理方法，无效事件抛出异常。

# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| TrustCertsContractEventParser | class | 解析区块链证书事件的Java类，处理插入和删除操作，使用MongoDB存储数据。 |



## 类 TrustCertsContractEventParser

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | TrustCertsContractEventParser |
| 说明 | 解析区块链证书事件的Java类，处理插入和删除操作，使用MongoDB存储数据。 |


### UML类图

```mermaid
classDiagram
    class AbstractParser {
        <<Abstract>>
        +parseContractEvent() void
    }

    class TrustCertsContractEventParser {
        -TrustCertsMongoRepo trustCertsMongoRepo
        -TrustCertsExtJSON extJSON
        +parseContractEvent() void
        -parseInsertEvent() void
        -parseDeleteBySerialNumberEvent() void
    }

    class TrustCertsMongoRepo {
        +save(TrustCerts entity) void
        +deleteBySerialNumber(String serialNumber) void
    }

    class TrustCertsExtJSON {
        // 扩展JSON数据结构
    }

    class TrustCerts {
        +String certId
        +String serialNumber
        +String certContent
        +String pCertId
        +String issuerOrg
        +String issuerCn
        +String subjectOrg
        +String subjectCn
        +String isCaCert
        +String isRootCert
        +String createdTime
        +String updatedTime
        +TrustCertsExtJSON extJson
    }

    class EventConstant.TrustCerts {
        <<Enumeration>>
        +INSERT_EVENT
        +DELETE_BY_SERIAL_NUMBER
    }

    AbstractParser <|-- TrustCertsContractEventParser
    TrustCertsContractEventParser --> TrustCertsMongoRepo : 依赖
    TrustCertsContractEventParser --> TrustCertsExtJSON : 依赖
    TrustCertsContractEventParser --> TrustCerts : 创建/操作
    TrustCertsContractEventParser --> EventConstant.TrustCerts : 事件类型判断
    TrustCertsMongoRepo ..> TrustCerts : 操作实体
```

该类图展示了TrustCertsContractEventParser继承自AbstractParser，用于解析区块链合约事件。它依赖TrustCertsMongoRepo进行数据库操作，使用TrustCertsExtJSON处理扩展数据，并根据EventConstant.TrustCerts枚举判断事件类型来执行插入或删除操作。TrustCerts类包含证书的完整字段结构，体现了从事件解析到数据存储的完整流程。


### 内部方法调用关系图

```mermaid
graph TD
    A["类TrustCertsContractEventParser"]
    B["属性: TrustCertsMongoRepo trustCertsMongoRepo"]
    C["属性: TrustCertsExtJSON extJSON"]
    D["方法: parseContractEvent()"]
    E["方法: parseInsertEvent()"]
    F["方法: parseDeleteBySerialNumberEvent()"]
    G["操作: 解析extJsonStr"]
    H["判断: eventBO.getEventName()"]
    I["调用: parseInsertEvent()"]
    J["调用: parseDeleteBySerialNumberEvent()"]
    K["异常: BusinessException"]
    L["操作: 创建TrustCerts对象并设置属性"]
    M["操作: trustCertsMongoRepo.save()"]
    N["操作: 获取serialNumber"]
    O["操作: trustCertsMongoRepo.deleteBySerialNumber()"]

    A --> B
    A --> C
    A --> D
    D --> G
    D --> H
    H -->|INSERT_EVENT| I
    H -->|DELETE_BY_SERIAL_NUMBER| J
    H -->|default| K
    I --> L
    L --> M
    J --> N
    N --> O
```

这段代码展示了一个区块链证书事件解析器，主要处理两种合约事件：INSERT_EVENT和DELETE_BY_SERIAL_NUMBER。当事件为INSERT_EVENT时，会创建TrustCerts对象并设置其属性后保存到MongoDB；当事件为DELETE_BY_SERIAL_NUMBER时，会根据序列号从MongoDB中删除对应记录。流程图中清晰展示了从事件解析到具体处理方法的完整调用链，包括属性初始化、JSON解析、事件类型判断和对应的数据库操作。

### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| trustCertsMongoRepo = BlockchainDataSyncApp.CONTEXT.getBean(TrustCertsMongoRepo.class) | TrustCertsMongoRepo | 从应用上下文中获取TrustCertsMongoRepo实例并赋值给保护变量。 |
| extJSON | TrustCertsExtJSON | 受保护的TrustCertsExtJSON扩展JSON对象。 |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| parseDeleteBySerialNumberEvent | void | 该方法解析删除事件，根据序列号从MongoDB仓库中删除对应证书。 |
| parseContractEvent | void | 解析合约事件方法，根据事件名称调用对应处理逻辑，无效事件抛出异常。 |
| parseInsertEvent | void | 解析插入事件，设置TrustCerts对象属性并保存到MongoDB。 |




