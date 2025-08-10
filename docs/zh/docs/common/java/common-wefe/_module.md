# 基础信息

|      |      |
|------|------|
| 名称 | common-wefe |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-wefe |
| 包名 | docs.common.java.common-wefe |
| 概述说明 | 服务检查框架实现分层健康检测，枚举模块定义联邦学习类型状态，配置管理模块统一处理多源连接，数据类型推断器分析字段类型。 |

# 说明

## 概述  
该模块是联邦学习系统的核心支撑框架，包含服务健康检查、枚举定义、配置管理和数据类型推断四大功能。采用分层抽象设计，关键接口包括AbstractCheckpoint（检查点）、AbstractConfigModel（配置模型）和Consumer（数据类型推断）。核心数据结构涵盖ServiceCheckPointOutput（检查结果）、11种ServiceType（服务类型枚举）和ColumnDataType（字段类型）。依赖Spring框架、JDBC驱动和云服务SDK。例如通过CheckpointManager并发检测UnionService连通性，或使用ColumnDataTypeInferrer推断字段类型。

## 主要业务场景  
模块支持联邦学习全生命周期管理：1) 服务健康检查采用哨兵模式，例如5秒超时检测；2) 枚举驱动状态机，如JobStatus控制任务流转；3) 工厂模式管理多数据源配置，例如生成特化数据库URL；4) 多线程推断字段类型（类似MapReduce）。典型流程包括配置校验→并行检查→结果聚合，例如UnionService检查失败时逐级上报。集成案例涵盖横向联邦学习（使用XGBoost算法）和云存储切换（如OSS凭证管理）。


### 包内部结构视图

None

# 文件列表

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| [com](src/main/java/com/_module.md) | folder | 服务检查框架实现分层健康检测，枚举模块定义联邦学习类型状态，配置管理模块统一处理多源连接，数据类型推断器分析字段类型。 |


