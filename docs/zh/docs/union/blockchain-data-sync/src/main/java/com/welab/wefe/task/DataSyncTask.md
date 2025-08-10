# 基础信息

|      |      |
|------|------|
| 名称 | DataSyncTask |
| 编码语言 | .java |
| 代码路径 | WeFe/union/blockchain-data-sync/src/main/java/com/welab/wefe/task/DataSyncTask.java |
| 包名 | com.welab.wefe.task |
| 依赖项 | ['com.welab.wefe.bo.data.BlockInfoBO', 'com.welab.wefe.bo.data.EventBO', 'com.welab.wefe.common.data.mongodb.entity.union.BlockSyncContractHeight', 'com.welab.wefe.common.data.mongodb.entity.union.BlockSyncHeight', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.util.ThreadUtil', 'com.welab.wefe.constant.BlockConstant', 'com.welab.wefe.constant.SyncConstant', 'com.welab.wefe.exception.BusinessException', 'com.welab.wefe.parser.BlockInfoParser', 'com.welab.wefe.service.BlockSyncContractHeightService', 'com.welab.wefe.service.BlockSyncDetailInfoService', 'com.welab.wefe.service.BlockSyncHeightService', 'com.welab.wefe.service.TransactionResponseService', 'com.welab.wefe.tool.DataProcessor', 'com.welab.wefe.tool.DataSyncContext', 'com.welab.wefe.util.BlockUtil', 'org.apache.commons.collections4.CollectionUtils', 'org.apache.commons.lang.math.NumberUtils', 'org.fisco.bcos.sdk.BcosSDK', 'org.fisco.bcos.sdk.client.Client', 'org.fisco.bcos.sdk.client.protocol.response.BcosBlock', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.beans.BeanUtils', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.beans.factory.annotation.Value', 'org.springframework.stereotype.Component', 'java.math.BigInteger', 'java.util.ArrayList', 'java.util.List'] |
| 概述说明 | DataSyncTask类用于同步区块链数据，包含组ID配置、微信通知URL，通过多线程按组同步区块数据，处理异常并记录同步状态。 |

# 说明

DataSyncTask是一个用于数据同步的组件类，通过注入多个服务和配置参数实现区块链数据同步功能。主要包含startTask方法启动同步任务，检查配置的群组ID并异步执行CrawlRunner。CrawlRunner是一个内部类，负责持续同步指定群组的区块数据，包括查询已同步区块、处理新区块、过滤已同步合约事件等。同步过程中会记录日志、处理异常，并通过相关服务保存同步结果和错误信息。整体实现了高效、稳定的区块链数据同步机制。

# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| DataSyncTask | class | DataSyncTask类是一个数据同步任务组件，通过多线程同步区块链数据，包含错误处理和过滤已同步事件功能。 |



## 类 DataSyncTask

|      |      |
|------|------|
| 访问范围 | @Component;public |
| 类型 | class |
| 名称 | DataSyncTask |
| 说明 | DataSyncTask类是一个数据同步任务组件，通过多线程同步区块链数据，包含错误处理和过滤已同步事件功能。 |


### UML类图

```mermaid
classDiagram
    class DataSyncTask {
        -Logger LOG
        -BcosSDK bcosSDK
        -BlockSyncHeightService blockSyncHeightService
        -BlockSyncContractHeightService blockSyncContractHeightService
        -BlockSyncDetailInfoService blockSyncDetailInfoService
        -TransactionResponseService transactionResponseService
        -String dataSyncGroupId
        -String wechatUrl
        +startTask()
        +CrawlRunner~inner~
    }

    class CrawlRunner {
        -int groupId
        -Client client
        +CrawlRunner(int groupId)
        +run()
        -startSync(long blockNumber) void
        -filterBlockInfoBO(BlockInfoBO blockInfoBO) BlockInfoBO
    }

    class BcosSDK {
        <<Interface>>
        +getClient(int groupId) Client
    }

    class BlockSyncHeightService {
        <<Interface>>
        +findByGroupId(String groupId) BlockSyncHeight
        +sendErrorMsg(int groupId, long blockNumber, Exception e) void
        +save(BlockInfoBO blockInfoBO) void
    }

    class BlockSyncContractHeightService {
        <<Interface>>
        +findByGroupIdAndContractName(String groupId, String contractName) BlockSyncContractHeight
        +save(BlockInfoBO blockInfoBO) void
    }

    class BlockSyncDetailInfoService {
        <<Interface>>
        +saveBlockDetailInfo(BlockInfoBO blockInfoBO) void
    }

    class TransactionResponseService {
        <<Interface>>
        +save(BlockInfoBO blockInfoBO) void
    }

    DataSyncTask --> BcosSDK : 依赖
    DataSyncTask --> BlockSyncHeightService : 依赖
    DataSyncTask --> BlockSyncContractHeightService : 依赖
    DataSyncTask --> BlockSyncDetailInfoService : 依赖
    DataSyncTask --> TransactionResponseService : 依赖
    DataSyncTask *-- CrawlRunner : 组合
    CrawlRunner --> BcosSDK : 调用
    CrawlRunner --> BlockSyncHeightService : 调用
    CrawlRunner --> BlockSyncContractHeightService : 调用
    CrawlRunner --> BlockSyncDetailInfoService : 调用
    CrawlRunner --> TransactionResponseService : 调用
```

这段代码展示了一个区块链数据同步任务的实现，主要包含DataSyncTask主类和其内部类CrawlRunner。DataSyncTask通过依赖注入获取多个服务接口实例，包括BcosSDK客户端和各类区块同步服务。CrawlRunner实现了Runnable接口，负责具体的区块同步逻辑，包括区块数据获取、过滤、处理和持久化。整个设计采用分层架构，主任务类负责调度，内部类处理具体业务逻辑，通过服务接口实现模块解耦。同步过程包含错误处理、重试机制和进度跟踪等功能，确保数据同步的可靠性和完整性。


### 内部方法调用关系图

```mermaid
graph TD
    A["类DataSyncTask"]
    B["属性: Logger LOG"]
    C["属性: BcosSDK bcosSDK"]
    D["属性: BlockSyncHeightService blockSyncHeightService"]
    E["属性: BlockSyncContractHeightService blockSyncContractHeightService"]
    F["属性: BlockSyncDetailInfoService blockSyncDetailInfoService"]
    G["属性: TransactionResponseService transactionResponseService"]
    H["属性: String dataSyncGroupId"]
    I["属性: String wechatUrl"]
    J["方法: startTask()"]
    K["内部类: CrawlRunner"]
    L["方法: run()"]
    M["方法: startSync(long blockNumber)"]
    N["方法: filterBlockInfoBO(BlockInfoBO blockInfoBO)"]

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
    K --> L
    K --> M
    K --> N

    J --> J1["检查dataSyncGroupId是否为空"]
    J1 -->|是| J2["记录警告日志并返回"]
    J1 -->|否| J3["分割groupIds并遍历"]
    J3 --> J4["检查是否为数字"]
    J4 -->|是| J5["创建CrawlRunner异步线程"]
    J4 -->|否| J6["跳过当前group"]

    L --> L1["获取client并创建dataSyncContext"]
    L1 --> L2["查询已同步区块高度"]
    L2 --> L3["获取当前最大区块高度"]
    L3 --> L4["检查是否需要等待新区块"]
    L4 -->|是| L5["休眠500ms后继续"]
    L4 -->|否| L6["遍历待同步区块"]
    L6 --> L7["调用startSync同步区块"]
    L7 -->|成功| L8["递增区块号"]
    L7 -->|业务异常| L9["发送错误消息并终止"]
    L7 -->|其他异常| L10["发送错误消息并重试"]

    M --> M1["重试10次获取区块数据"]
    M1 --> M2["解析区块信息"]
    M2 --> M3["过滤已同步合约事件"]
    M3 --> M4["处理区块数据"]
    M4 --> M5["保存合约高度"]
    M5 --> M6["保存区块详情"]
    M6 --> M7["保存区块高度"]
    M7 --> M8["保存交易响应"]

    N --> N1["复制BlockInfoBO"]
    N1 --> N2["过滤已同步事件"]
    N2 --> N3["返回过滤后对象"]
```

这段代码实现了一个区块链数据同步任务，主要包含DataSyncTask类及其内部类CrawlRunner。流程图展示了从任务启动到区块同步的完整流程：首先校验配置参数，然后对每个分组创建异步线程；在同步过程中会检查区块高度差异，通过重试机制获取区块数据，过滤已处理事件后保存各类信息。整个流程包含完善的异常处理和日志记录机制，通过多服务协作完成区块链数据的增量同步。

### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| blockSyncContractHeightService | BlockSyncContractHeightService | 自动注入区块同步合约高度服务实例。 |
| LOG = LoggerFactory.getLogger(DataSyncTask.class) | Logger | 定义DataSyncTask类的私有静态日志对象LOG。 |
| transactionResponseService | TransactionResponseService | 代码片段使用@Autowired注解自动注入TransactionResponseService实例。 |
| blockSyncHeightService | BlockSyncHeightService | 自动注入区块同步高度服务实例。 |
| blockSyncDetailInfoService | BlockSyncDetailInfoService | 代码片段使用@Autowired注解自动注入BlockSyncDetailInfoService服务实例。 |
| dataSyncGroupId | String | 代码片段定义了一个私有字符串变量dataSyncGroupId，其值通过@Value注解从配置项contract.data-sync-group-id注入。 |
| wechatUrl | String | 微信机器人URL配置项，通过@Value注入到私有变量wechatUrl中。 |
| bcosSDK | BcosSDK | 使用@Autowired自动注入BcosSDK实例。 |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| startTask | void | 方法检查数据同步组ID配置，若为空则警告并返回。否则分割组ID为数组，遍历每个ID，跳过非数字项，对有效ID启动异步爬取任务。 |




