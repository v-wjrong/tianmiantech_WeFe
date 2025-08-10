# 基础信息

|      |      |
|------|------|
| 名称 | common-data-mongodb |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-data-mongodb |
| 包名 | docs.common.java.common-data-mongodb |
| 概述说明 | MongoDB数据访问层提供CRUD和复杂查询功能，支持逻辑删除和时间戳约束。包含短信业务分类、供应商枚举管理。工具集支持链式查询构建和聚合操作。联邦学习平台实现日志、证书和数据治理。统一查询管理数据集和成员认证。连接管理模块动态注册MongoDB组件。 |

# 说明

## 概述  
该模块是联邦学习平台的核心数据管理组件，基于MongoDB实现多领域数据的统一存储与操作，类似数据总线模式。核心职责包括：1) 通过标准化CRUD接口管理20+业务实体（如证书、数据集）；2) 提供复杂查询构建工具和聚合操作支持；3) 统一连接管理与事务控制。  

接口规范分层设计：基础层（AbstractMongoModel/Repo）定义主键和序列化规则，业务层扩展特定操作（如版本控制）。关键数据结构含分页对象PageOutput、证书PEM内容、数据集权限模型等。外部依赖包括Spring Data MongoDB、QueryBuilder和MongoDB驱动。例如RealnameAuthAgreementTemplateMongoRepo实现乐观锁更新，QueryBuilder支持范围筛选。  

## 主要业务场景  
模块支撑四大典型场景：1) 数据治理（如DataSet权限控制），类似RBAC模型；2) 操作审计（记录API调用日志）；3) 联邦资源检索（多条件分页查询）；4) 证书全生命周期管理。业务流程涵盖：通过枚举选择短信模板、链式构建更新条件、聚合管道处理数据集权限。  

交互模式以DTO传输和API组合为主，例如ImageDataSetMongoReop联合标签表查询，AccountMongoRepo实现活跃度检测。功能完整性体现在覆盖数据全生命周期（元数据→使用统计），典型应用包括任务配置时的资源选择器、节点资质校验等。API类型含CRUD操作（如certStatus更新）和配置类（@Configuration），集成案例可见区块同步服务的高度记录。


### 包内部结构视图

None

# 文件列表

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| [com](src/main/java/com/_module.md) | folder | MongoDB数据访问层提供CRUD和复杂查询功能，支持逻辑删除和时间戳约束。包含短信业务分类、供应商枚举管理。工具集支持链式查询构建和聚合操作。联邦学习平台实现日志、证书和数据治理。统一查询管理数据集和成员认证。连接管理模块动态注册MongoDB组件。 |


