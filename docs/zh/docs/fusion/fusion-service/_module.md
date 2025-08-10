# 基础信息

|      |      |
|------|------|
| 名称 | fusion-service |
| 编码语言 | .java |
| 代码路径 | WeFe/fusion/fusion-service |
| 包名 | docs.fusion.fusion-service |
| 概述说明 | 联邦学习平台核心系统，含控制、数据、任务模块，支持初始化、数据管理、任务调度全流程。分层架构设计，统一接口规范，关键数据结构和多服务组件集成。 |

# 说明

## 概述  
该模块是联邦学习平台的核心管理系统，采用分层架构设计，集成系统控制、数据管理、任务调度和隐私计算功能。核心职责包括：1)通过分层存储系统（MySQL/MergeTree）实现数据持久化；2)基于PSI（隐私集合求交）算法保障跨机构数据安全对齐；3)提供全生命周期管理工具集（布隆过滤器/主键生成等）。接口规范统一采用JPA注解和RESTful风格，例如AbstractApi基类派生各类API，@Query实现扩展查询。关键数据结构涵盖分页结果集、加密业务实体（如GlobalConfigMysqlModel）和PSI执行参数（e/N/d）。外部依赖包括Spring Data JPA、RSA加密组件、连接池管理（如HikariCP）和多种数据库驱动（MySQL/Hive/Impala）。

## 主要业务场景  
模块支持联邦学习全流程管理，典型工作流为：1)系统初始化（生成RSA密钥/校验memberName）；2)数据准备（DatasetApi管理CSV/Excel解析）；3)安全计算（PsiClientActuator执行加密分片）；4)结果回调（TaskResultManager动态建表存储）。交互模式融合生产者-消费者模型（批量处理10,000行数据）和状态机驱动（TaskStatus管理7种状态）。功能完整性体现在：加密校验（≤5字段组合）、线程安全操作（ConcurrentHashMap管理任务）和异常处理链（StatusCodeWithException）。集成案例覆盖从基础配置（DataSourceConfig多数据源）到复杂业务（RSA-PSI算法切换），类似分布式ETL控制台。


### 包内部结构视图

None

# 文件列表

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| [com](src/main/java/com/_module.md) | folder | 联邦学习平台核心系统，含控制、数据、任务模块，支持初始化、数据管理、任务调度全流程。分层架构设计，统一接口规范，关键数据结构和多服务组件集成。 |


