# 基础信息

|      |      |
|------|------|
| 名称 | repository |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/database/repository |
| 包名 | docs.board.board-service.src.main.java.com.welab.wefe.board.service.database.repository |
| 概述说明 | Spring Data JPA实现的资源管理仓库层，统一管理各类数据资源，提供CRUD扩展功能。包含数据清理、状态维护、使用统计等业务场景，支持原生SQL和事务操作。 |

# 说明

## 概述  
该模块是基于Spring Data JPA构建的通用数据访问层，核心职责是统一管理各类业务实体（如数据集、任务、消息等）的持久化操作，类似企业级数据中台架构。接口规范遵循JPA标准，通过BaseRepository基类扩展基础CRUD能力，支持原生SQL查询（例如countByName统计同名记录）、批量更新和分页转换等特性。关键数据结构包括40+种MySqlModel实体类（如TaskMySqlModel、MessageMysqlModel等），均采用String类型主键。外部依赖仅Spring Data JPA框架，通过@Transactional和@Modifying保障事务安全。例如ProjectDataSetRepository实现数据集状态批量更新时自动清除持久化上下文。

## 主要业务场景  
模块支撑全业务生命周期管理，采用仓库模式统一交互，类似资源管理中心设计。典型流程包括：数据预处理（ImageDataSetSampleRepository管理标注样本）、任务调度（JobRepository跟踪运行状态）、消息处理（MessageQueueRepository维护消息队列）和权限控制（AccountRepository管理用户状态）。交互模式通过JPA接口暴露，例如ProjectFlowRepository提供流程置顶/取消操作，MemberChatRepository实现消息状态更新。API类型涵盖基础CRUD（90%）、定制查询（如listAllTags）和业务操作（如disableDataSetWhenMemberExist），集成案例包括事务性删除（ChatUnreadMessageRepository）和多条件检索（TaskRepository.findTaskWithGridSearch）。


### 包内部结构视图

```mermaid
graph TD
    repository --> data_resource
    repository --> fusion
    repository --> base
    repository --> TaskProgressRepository.java
    repository --> DataSourceRepository.java
    repository --> ChatLastAccountRepository.java
    repository --> ChatUnreadMessageRepository.java
    repository --> DataSetColumnRepository.java
    repository --> ModelOotRecordRepository.java
    repository --> OperationLogRepository.java
    repository --> JobMemberRepository.java
    repository --> GlobalConfigRepository.java
    repository --> ProjectMemberAuditRepository.java
    repository --> DataOutputInfoRepository.java
    repository --> OutputModelRepository.java
    repository --> PartnerConfigRepository.java
    repository --> TaskRepository.java
    repository --> CertInfoRepository.java
    repository --> FeatureJobMemberRepository.java
    repository --> MemberChatRepository.java
    repository --> FlowActionLogRepository.java
    repository --> BlacklistRepository.java
    repository --> FlowTemplateRepository.java
    repository --> MessageRepository.java
    repository --> CertKeyInfoRepository.java
    repository --> AccountRepository.java
    repository --> TrackingMetricRepository.java
    repository --> ImageDataSetSampleRepository.java
    repository --> ProjectFlowNodeRepository.java
    repository --> ProjectMemberRepository.java
    repository --> ProjectDataSetRepository.java
    repository --> FlowActionQueueRepository.java
    repository --> MessageQueueRepository.java
    repository --> TaskContextRepository.java
    repository --> JobRepository.java
    repository --> CertRequestInfoRepository.java
    repository --> RoleCountsRepository.java
    repository --> TaskResultRepository.java
    repository --> VerificationCodeRepository.java
    repository --> ProjectFlowRepository.java
    repository --> ProjectRepository.java
    data_resource --> BloomFilterRepository.java
    data_resource --> DataResourceUploadTaskRepository.java
    data_resource --> DataResourceRepository.java
    data_resource --> TableDataSetRepository.java
    data_resource --> ImageDataSetRepository.java
    fusion --> ExportProgressRepository.java
    fusion --> FieldInfoRepository.java
    fusion --> FusionActuatorInfoRepository.java
    fusion --> BloomFilterTaskRepository.java
    fusion --> FusionResultRepository.java
    fusion --> FusionTaskRepository.java
    fusion --> BloomFilterColumnRepository.java
    base --> BaseRepositoryFactoryBean.java
    base --> RepositoryManager.java
    base --> BaseRepositoryImpl.java
    base --> BaseRepository.java
```

该流程图展示了一个Java项目中的数据库仓库(repository)结构，包含data_resource、fusion和base三个子目录，以及大量直接位于repository目录下的Java文件。子目录中又包含各自的实现类，整体呈现多层级树状结构，反映了项目对数据访问层的模块化设计。

# 文件列表

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| [TaskProgressRepository.java](TaskProgressRepository.md) | file | 任务进度仓库接口，继承基础仓库，操作任务进度MySQL模型，主键类型为字符串。 |
| [DataSourceRepository.java](DataSourceRepository.md) | file | 这是一个Spring Data JPA仓库接口，继承基础仓库并定义了一个原生SQL查询方法，用于按名称统计数据源数量。 |
| [ChatLastAccountRepository.java](ChatLastAccountRepository.md) | file | 这是一个Spring的Repository接口，用于操作ChatLastAccountMysqlModel数据，提供按accountId和liaisonAccountId删除记录的方法。 |
| [ChatUnreadMessageRepository.java](ChatUnreadMessageRepository.md) | file | ChatUnreadMessageRepository接口继承BaseRepository，提供按发送和接收账号查询未读消息及删除记录的方法。 |
| [DataSetColumnRepository.java](DataSetColumnRepository.md) | file | 这是一个Spring Data JPA仓库接口，用于操作数据集列模型。它继承基础仓库并定义了一个删除方法，根据数据集ID删除记录，支持事务和自动清除缓存。 |
| [ModelOotRecordRepository.java](ModelOotRecordRepository.md) | file | 这是一个Spring的Repository接口，继承自BaseRepository，用于操作ModelOotRecordMysqlModel实体类，主键类型为String。 |
| [OperationLogRepository.java](OperationLogRepository.md) | file | 操作日志仓库接口，继承基础仓库类，操作日志模型为MySQL类型，主键为字符串。 |
| [JobMemberRepository.java](JobMemberRepository.md) | file | JobMemberRepository接口继承BaseRepository，操作JobMemberMySqlModel实体，主键类型为String。 |
| [GlobalConfigRepository.java](GlobalConfigRepository.md) | file | 这是一个Spring的Repository接口，继承BaseRepository，用于操作GlobalConfigMysqlModel数据，提供按group字段查询的功能。 |
| [ProjectMemberAuditRepository.java](ProjectMemberAuditRepository.md) | file | 项目成员审核仓库接口，继承基础仓库，提供删除指定成员审核记录功能，包括其审核和被审核记录，通过原生SQL实现。 |
| [DataOutputInfoRepository.java](DataOutputInfoRepository.md) | file | 数据输出信息仓库接口，继承基础仓库类，操作数据输出信息MySQL模型，主键类型为字符串。 |
| [OutputModelRepository.java](OutputModelRepository.md) | file | 这是一个Spring Data JPA仓库接口，继承基础仓库类，用于操作OutputModelMysqlModel实体，主键类型为String。 |
| [PartnerConfigRepository.java](PartnerConfigRepository.md) | file | PartnerConfigRepository接口继承BaseRepository，提供按memberId查询PartnerConfigMysqlModel的方法。 |
| [TaskRepository.java](TaskRepository.md) | file | TaskRepository接口扩展BaseRepository，包含两个原生SQL查询方法：findOne按jobId、flowNodeId和role查找最新任务；findTaskWithGridSearch查找非arbiter角色且需要网格搜索的任务列表。 |
| [CertInfoRepository.java](CertInfoRepository.md) | file | CertInfoRepository接口定义了两个方法：updateStatus根据ID更新状态，resetCert重置所有证书状态。均使用原生SQL并支持事务。 |
| [FeatureJobMemberRepository.java](FeatureJobMemberRepository.md) | file | 这是一个Spring的仓库接口，继承基础仓库类，用于管理JobMemberMySqlModel类型数据，主键为String类型。 |
| [MemberChatRepository.java](MemberChatRepository.md) | file | 成员聊天仓库接口，包含查询双方聊天记录、获取聊天列表及更新消息状态的方法。 |
| [FlowActionLogRepository.java](FlowActionLogRepository.md) | file | 这是一个Spring的仓库接口，继承基础仓库类，用于操作FlowActionLogMySqlModel类型数据，主键为String类型。 |
| [BlacklistRepository.java](BlacklistRepository.md) | file | 这是一个Spring Data JPA仓库接口，继承基础仓库类，提供按成员ID查询黑名单数据的方法。 |
| [FlowTemplateRepository.java](FlowTemplateRepository.md) | file | 这是一个Spring的仓库接口，继承基础仓库类，用于操作FlowTemplateMySqlModel数据，主键类型为String。 |
| [MessageRepository.java](MessageRepository.md) | file | MessageRepository接口定义了两个方法：completeApplyDataResourceTodo更新指定项目和数据资源的待办状态为已完成和已读；completeApplyJoinProjectTodo更新指定关联ID的加入项目待办状态为已完成和已读。均使用原生SQL并支持事务。 |
| [CertKeyInfoRepository.java](CertKeyInfoRepository.md) | file | 这是一个Spring的JPA仓库接口，继承基础仓库类，用于操作CertKeyInfoMysqlModel数据模型，主键类型为String。 |
| [AccountRepository.java](AccountRepository.md) | file | AccountRepository接口提供账号管理功能，包括按手机号查询、取消管理员权限、更新最后操作时间、禁用90天未活动账号、注销180天未活动账号及更新UI配置。 |
| [TrackingMetricRepository.java](TrackingMetricRepository.md) | file | 这是一个Spring框架的仓库接口，继承基础仓库类，用于操作TrackingMetricMysqlModel数据模型，主键类型为String。 |
| [ImageDataSetSampleRepository.java](ImageDataSetSampleRepository.md) | file | ImageDataSetSampleRepository接口扩展BaseRepository，提供删除、查询标签列表及统计样本数量的方法，支持数据集ID操作。 |
| [ProjectFlowNodeRepository.java](ProjectFlowNodeRepository.md) | file | 项目流程节点仓库接口，提供按流程ID和节点ID查询节点方法，以及删除指定流程中不在给定节点ID列表中的节点功能。 |
| [ProjectMemberRepository.java](ProjectMemberRepository.md) | file | 项目成员仓库接口，继承基础仓库，定义查询方法获取所有合作成员ID。 |
| [ProjectDataSetRepository.java](ProjectDataSetRepository.md) | file | ProjectDataSetRepository接口定义：1.成员退出时禁用数据集；2.查询项目中可用数据集；3.统计待审核数据集数量。 |
| [FlowActionQueueRepository.java](FlowActionQueueRepository.md) | file | 这是一个Spring框架的仓库接口，继承基础仓库类，用于操作FlowActionQueueMySqlModel类型数据，主键为String类型。 |
| [MessageQueueRepository.java](MessageQueueRepository.md) | file | 消息队列仓库接口，继承基础仓库，操作消息队列MySQL模型，主键类型为字符串。 |
| [TaskContextRepository.java](TaskContextRepository.md) | file | 这是一个Spring的Repository接口，继承自BaseRepository，用于操作TaskContextMySqlModel类型的数据，主键类型为String。 |
| [JobRepository.java](JobRepository.md) | file | JobRepository接口扩展BaseRepository，提供三个原生SQL查询方法：按jobId和role查找任务，按flowId和role查找最新任务，统计未结束任务数量。 |
| [CertRequestInfoRepository.java](CertRequestInfoRepository.md) | file | 接口CertRequestInfoRepository继承BaseRepository，用于操作CertRequestInfoMysqlModel数据，主键类型为String。 |
| [RoleCountsRepository.java](RoleCountsRepository.md) | file | 接口RoleCountsRepository定义，无具体方法。 |
| [TaskResultRepository.java](TaskResultRepository.md) | file | 这是一个Spring的TaskResultRepository接口，继承BaseRepository，用于操作TaskResultMySqlModel类型数据，主键为String类型。 |
| [VerificationCodeRepository.java](VerificationCodeRepository.md) | file | 这是一个Spring的Repository接口，继承自BaseRepository，用于操作VerificationCodeMysqlModel类型的数据，主键类型为String。 |
| [ProjectFlowRepository.java](ProjectFlowRepository.md) | file | ProjectFlowRepository接口提供项目流程状态统计、置顶及取消置顶功能，使用原生SQL查询和更新操作。 |
| [ProjectRepository.java](ProjectRepository.md) | file | ProjectRepository接口包含查询非管理员创建的10天前的项目、获取项目最后启动时间、按名称或ID查询项目、置顶及取消置顶功能。 |
| [base](base/_module.md) | package | BaseRepositoryFactoryBean定义泛型工厂Bean，扩展JPA仓库创建流程。RepositoryManager缓存模型与仓库映射，支持扫描与手动注册。BaseRepositoryImpl实现通用JPA操作，含查询、更新、分页及SQL功能。BaseRepository接口扩展标准JPA功能，支持字段查询、更新及事务处理。 |
| [fusion](fusion/_module.md) | package | 定义了多个Spring数据仓库接口，均继承BaseRepository，操作不同实体类，主键为String。包含CRUD操作和特定查询方法，如按业务ID查询最新记录或按ID删除记录。 |
| [data_resource](data_resource/_module.md) | package | Spring仓库接口定义：BloomFilterRepository操作布隆过滤器模型；DataResourceUploadTaskRepository管理上传任务，含清理和超时处理；DataResourceRepository提供标签查询、计数和更新方法；TableDataSetRepository和ImageDataSetRepository分别操作表数据和图像数据模型。 |


