# 基础信息

|      |      |
|------|------|
| 名称 | blockchain-data-sync |
| 编码语言 | .java |
| 代码路径 | WeFe/union/blockchain-data-sync |
| 包名 | docs.union.blockchain-data-sync |
| 概述说明 | 区块链数据同步系统核心组件，包含解析器、工具类、服务层及配置管理。解析器将合约事件转为MongoDB操作，工具类提供辅助功能，服务层处理数据持久化，配置管理初始化环境。支持多线程同步，确保数据一致性。 |

# 说明

## 概述  
该模块是区块链数据同步系统的核心组件，采用分层架构设计，负责链上合约事件的解析、转换与持久化。核心职责包括：通过抽象工厂模式实现事件解析（如MemberContractEventParser）、线程安全的数据同步管理（如SyncConstant）以及工具集支持（如AbiUtil）。关键数据结构涵盖EventBO业务对象、BlockInfoBO区块信息及ContractABIDefinition等元数据。外部依赖包括MongoDB、区块链节点SDK（BcosBlock）、Java标准库及微信通知API。例如通过BlockSyncHeightService实现区块高度幂等更新，ClassPathScanHandler动态加载解析器类。

## 主要业务场景  
模块支持多线程环境下的区块链数据全生命周期管理，类似ETL管道与事件总线混合模式。典型流程为：InitListener初始化环境→DataSyncTask同步区块→DataProcessor路由事件→子类Parser处理业务→MongoDB持久化。主要处理三类场景：实体状态变更（如成员公钥更新）、元数据维护（如ABI解析）和资源权限管理（如数据集标签控制）。交互模式统一通过parseContractEvent等静态方法驱动，例如UnionNodeContractEventParser处理节点状态变更，BloomFilterContractEventParser维护布隆过滤器参数。API类型包含工厂方法、扫描接口和数据处理三类，集成案例展示线程安全的高度更新与合约解析器自动发现。


### 包内部结构视图

None

# 文件列表

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| [com](src/main/java/com/_module.md) | folder | 区块链数据同步系统核心组件，包含解析器、工具类、服务层及配置管理。解析器将合约事件转为MongoDB操作，工具类提供辅助功能，服务层处理数据持久化，配置管理初始化环境。支持多线程同步，确保数据一致性。 |


