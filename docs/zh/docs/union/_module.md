# 基础信息

|      |      |
|------|------|
| 名称 | union |
| 编码语言 | .java |
| 代码路径 | WeFe/union |
| 包名 | docs.union |
| 概述说明 | 联盟链管理模块提供成员、数据、合约及监控管理，采用分层接口设计，依赖FISCO BCOS和Spring。数据同步模块负责链上事件解析与持久化，支持多线程ETL流程，依赖MongoDB和节点SDK。 |

# 说明

## 概述  
该模块群是联盟链环境下的综合管理系统，核心职责包括成员生命周期管理、数据资源操作、智能合约封装及区块链数据同步，类似企业级RBAC与区块链ETL管道的结合体。接口规范采用分层设计，包含AbstractApi基类继承、@Api注解定义、标准化DTO封装及工厂模式解析器（如MemberContractEventParser）。关键数据结构涵盖成员信息（MemberQueryOutput）、事件对象（EventBO）、智能合约返回值（Tuple）及区块元数据（BlockInfoBO）。外部依赖涉及FISCO BCOS SDK、国密算法库、MongoDB、Spring框架及微信通知API。例如MemberService管理成员注册流程，BlockSyncHeightService实现区块高度同步，AbiUtil处理合约ABI解析。

## 主要业务场景  
模块支持四大典型流程：1)成员全周期管理（注册→认证→状态更新），通过智能合约与MemberService联动；2)数据资源CRUD与权限控制，采用"本地校验+链上操作"双阶段模式；3)区块链数据同步，类似ETL管道实现InitListener→DataSyncTask→Parser→持久化流程；4)系统监控与健康检查。交互模式包括RESTful API（如member/realname/auth）、静态工具类（FileCheckerUtil）和事件驱动（如UnionNodeContractEventParser）。典型应用涵盖特征集查询、文件同步及证书状态流转，功能完整性体现在细粒度权限、异构数据转换（MapperUtil）和线程安全的高度更新机制。


### 包内部结构视图

None

# 文件列表

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| [blockchain-data-sync](blockchain-data-sync/src/main/java/com/_module.md) | module | 区块链数据同步系统核心组件，包含解析器、工具类、服务层及配置管理。解析器将合约事件转为MongoDB操作，工具类提供辅助功能，服务层处理数据持久化，配置管理初始化环境。支持多线程同步，确保数据一致性。 |
| [union-service](union-service/src/main/java/com/_module.md) | module | 联盟服务模块群提供多维度管理能力，包括会员生命周期、数据资源操作、公共服务及监控。采用RESTful接口，统一继承AbstractApi基类，关键结构含MemberOutput等。支持四大场景：会员管理、数据CRUD、公共服务及健康检测。依赖MemberService等组件，集成智能合约与区块链技术，实现联邦学习数据协同与权限控制。 |


