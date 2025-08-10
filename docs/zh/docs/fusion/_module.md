# 基础信息

|      |      |
|------|------|
| 名称 | fusion |
| 编码语言 | .java |
| 代码路径 | WeFe/fusion |
| 包名 | docs.fusion |
| 概述说明 | 联邦学习核心管理系统，集成数据持久化、隐私计算（PSI算法）和任务调度，支持全生命周期管理。采用分层架构，依赖Spring Data JPA和多种数据库驱动。典型流程包括初始化、数据准备、安全计算和结果回调。 |

# 说明

## 概述  
该模块是联邦学习平台的核心管理系统，采用分层架构设计，集成系统控制、数据管理、任务调度和隐私计算功能。核心职责包括：1)通过分层存储系统（如MySQL/MergeTree）实现数据持久化；2)基于PSI（隐私集合求交）算法保障跨机构数据安全对齐；3)提供全生命周期管理工具集（如布隆过滤器/主键生成）。接口规范统一采用JPA注解和RESTful风格，例如AbstractApi基类派生各类API，@Query实现扩展查询。关键数据结构涵盖分页结果集、加密业务实体（如GlobalConfigMysqlModel）和PSI执行参数（e/N/d）。外部依赖包括Spring Data JPA、RSA加密组件、连接池管理（如HikariCP）和多种数据库驱动（MySQL/Hive/Impala）。  

该模块同时实现隐私保护集合交集(PSI)协议的双端逻辑与联邦学习支持组件，核心职责包括安全数据对齐（类似盲签名流程）、布隆过滤器操作及任务状态管理。接口规范涵盖Server/Client抽象基类、枚举定义和DTO传输模型，例如dataTransform数据转换和generateBlindingFactor元数据下载。关键数据结构含BigInteger加密参数、BitSet位集、BloomFilterDto传输对象及PSIActuatorRole等枚举。外部依赖涉及JObject序列化框架、RSA-PSI算法和Java密码学组件。例如ActuatorCache管理执行器映射，BloomFilterUtils简化IO操作。  

## 主要业务场景  
模块支持联邦学习全流程管理，典型工作流为：1)系统初始化（生成RSA密钥/校验memberName）；2)数据准备（DatasetApi管理CSV/Excel解析）；3)安全计算（PsiClientActuator执行加密分片）；4)结果回调（TaskResultManager动态建表存储）。交互模式融合生产者-消费者模型（批量处理10,000行数据）和状态机驱动（TaskStatus管理7种状态）。功能完整性体现在：加密校验（≤5字段组合）、线程安全操作（ConcurrentHashMap管理任务）和异常处理链（StatusCodeWithException）。集成案例覆盖从基础配置（DataSourceConfig多数据源）到复杂业务（RSA-PSI算法切换），类似分布式ETL控制台。  

典型流程还遵循Client初始化→元数据交换→分桶加密→Server匹配→结果回传，采用类似MapReduce的多线程分页处理。完整功能覆盖数据预处理（如parseAndMatch）、加密转换（RSA/DH算法）、状态协调（FusionTaskStatus枚举）和过滤器持久化（writeTo/readFrom）。交互模式基于角色（server/client）和状态驱动（如Progress.Ready触发执行），API类型包括基础操作（add/contains）、密码学功能（generateKeys）和线程池任务提交。例如MD5哈希确保数据一致性，AlgorithmType.DH支持密钥交换，DTO模式实现跨节点传输。


### 包内部结构视图

None

# 文件列表

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| [fusion-core](fusion-core/src/main/java/com/_module.md) | module | 模块实现隐私保护集合交集(PSI)协议，含Server/Client基类、数据转换和元数据处理，依赖RSA-PSI算法和JObject序列化。布隆过滤器模块支持高效操作与持久化，集成密码学工具和线程池管理。枚举模块定义联邦学习关键维度如任务状态和算法类型。DTO模块封装布隆过滤器及元数据，支持PSI协议组件序列化传输。 |
| [fusion-service](fusion-service/src/main/java/com/_module.md) | module | 联邦学习平台核心系统，含控制、数据、任务模块，支持初始化、数据管理、任务调度全流程。分层架构设计，统一接口规范，关键数据结构和多服务组件集成。 |


