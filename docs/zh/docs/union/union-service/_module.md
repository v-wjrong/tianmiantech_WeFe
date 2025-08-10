# 基础信息

|      |      |
|------|------|
| 名称 | union-service |
| 编码语言 | .java |
| 代码路径 | WeFe/union/union-service |
| 包名 | docs.union.union-service |
| 概述说明 | 联盟服务模块群提供多维度管理能力，包括会员生命周期、数据资源操作、公共服务及监控。采用RESTful接口，统一继承AbstractApi基类，关键结构含MemberOutput等。支持四大场景：会员管理、数据CRUD、公共服务及健康检测。依赖MemberService等组件，集成智能合约与区块链技术，实现联邦学习数据协同与权限控制。 |

# 说明

## 概述  
该模块群核心职责为提供联盟链环境下的多维度管理能力，涵盖成员生命周期管理、数据资源操作、智能合约封装及系统监控，类似企业级RBAC与数据中台的结合体。接口规范采用分层设计，包含AbstractApi基类继承、@Api注解定义和标准化DTO封装（如BaseInput/MemberOutput），支持RESTful交互与Getter/Setter模式。关键数据结构包括成员信息（MemberQueryOutput）、数据资源（DataResourcePutInput）、智能合约返回值（Tuple）及枚举状态（CertStatusEnums）。外部依赖涉及FISCO BCOS SDK、国密算法库、MongoDB驱动及Spring框架。例如MemberContract管理成员全生命周期，FileUploadApi处理文件凭证，UnionNodeConfigCache维护SM2密钥。

## 主要业务场景  
模块支持四大典型流程：1)成员全周期管理（注册→认证→状态更新），通过MemberService和智能合约联动，类似CRM与区块链融合；2)数据资源CRUD与权限控制，采用"本地校验+链上操作"双阶段模式，如DataSetService控制分级公开；3)智能合约封装场景（如MemberContract），支持ECDSA/SM2双算法及事件订阅；4)系统监控与日志，类似探针机制通过UnionAvailableApi检测服务状态。交互模式涵盖RESTful API（member/realname/auth）、静态工具类（FileCheckerUtil）和事件驱动（合约事件总线）。典型应用包括联合建模时特征集查询（QueryApi）、文件同步（UploadFileSyncToUnionTask）及证书状态流转（CertStatusEnums）。功能完整性体现在细粒度权限、健康检查链和异构数据转换（如MapperUtil处理时间格式）。


### 包内部结构视图

None

# 文件列表

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| [com](src/main/java/com/_module.md) | folder | 联盟服务模块群提供多维度管理能力，包括会员生命周期、数据资源操作、公共服务及监控。采用RESTful接口，统一继承AbstractApi基类，关键结构含MemberOutput等。支持四大场景：会员管理、数据CRUD、公共服务及健康检测。依赖MemberService等组件，集成智能合约与区块链技术，实现联邦学习数据协同与权限控制。 |


