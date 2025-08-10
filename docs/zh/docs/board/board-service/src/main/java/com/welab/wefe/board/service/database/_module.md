# 基础信息

|      |      |
|------|------|
| 名称 | database |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/database |
| 包名 | docs.board.board-service.src.main.java.com.welab.wefe.board.service.database |
| 概述说明 | 基于Spring Data JPA的通用数据访问层，统一管理业务实体持久化，支持CRUD、批量更新和分页。关键数据结构含40+实体类，依赖Spring Data JPA保障事务安全。支撑全业务生命周期管理，涵盖数据预处理、任务调度等场景。 |

# 说明

## 概述  
该模块是联邦学习平台的核心数据持久化层，基于Spring Data JPA构建，采用企业级数据中台架构统一管理多领域业务实体（如数据集、任务、证书等）。接口规范遵循JPA标准，通过BaseRepository扩展CRUD能力，支持原生SQL查询、批量更新和分页转换（例如countByName统计同名记录）。关键数据结构形成三大体系：证书管理类（如CertKeyInfoMysqlModel）、联邦学习类（如JobMySqlModel）和数据资源类（如TableDataSetMysqlModel），均采用String类型主键。外部依赖集中于MySQL、Spring Data JPA和加密组件（如DatabaseEncryptConverter），通过@Transactional保障事务安全。例如GlobalConfigMysqlModel实现配置项加密存储，ProjectDataSetRepository支持数据集状态批量更新。

## 主要业务场景  
模块支撑联邦学习全流程与周边系统协同，类似工作流引擎与消息总线结合体。典型场景包括：数据预处理（ImageDataSetSampleRepository管理标注样本）、任务调度（JobRepository监控进度）、证书签发（CA审核→密钥存储）和消息处理（MessageQueueRepository维护待办事项）。交互模式呈现资源型（管理标注数据）、任务型（跟踪流程节点）和消息型（处理状态更新）三维度，通过JPA接口暴露操作（例如ProjectFlowRepository提供流程置顶功能）。API类型涵盖基础CRUD（90%）、定制查询（如listAllTags）和业务操作（如disableDataSetWhenMemberExist），集成案例包括事务性删除（ChatUnreadMessageRepository）和多条件检索（TaskRepository.findTaskWithGridSearch）。


### 包内部结构视图

```mermaid
graph TD
    database --> repository
    database --> entity
    database --> DataSourceConfig.java
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
    entity --> cert
    entity --> data_resource
    entity --> job
    entity --> chat
    entity --> data_set
    entity --> flow
    entity --> fusion
    entity --> base
    entity --> MessageMysqlModel.java
    entity --> PartnerConfigMysqlModel.java
    entity --> OutputModelMysqlModel.java
    entity --> GlobalConfigMysqlModel.java
    entity --> BlacklistMysqlModel.java
    entity --> OperationLogMysqlModel.java
    entity --> VerificationCodeMysqlModel.java
    entity --> DataSourceMysqlModel.java
    entity --> TrackingMetricMysqlModel.java
    entity --> AccountMysqlModel.java
    entity --> DataOutputInfoMysqlModel.java
    cert --> CertKeyInfoMysqlModel.java
    cert --> CertRequestInfoMysqlModel.java
    cert --> CertInfoMysqlModel.java
    data_resource --> DataResourceUploadTaskMysqlModel.java
    data_resource --> BloomFilterMysqlModel.java
    data_resource --> TableDataSetMysqlModel.java
    data_resource --> DataResourceMysqlModel.java
    data_resource --> ImageDataSetMysqlModel.java
    job --> ModelOotRecordMysqlModel.java
    job --> TaskMySqlModel.java
    job --> JobMemberMySqlModel.java
    job --> TaskResultMySqlModel.java
    job --> ProjectMemberAuditMySqlModel.java
    job --> JobMySqlModel.java
    job --> ProjectFlowNodeMySqlModel.java
    job --> ProjectFlowMySqlModel.java
    job --> ProjectDataSetMySqlModel.java
    job --> TaskProgressMysqlModel.java
    job --> TaskContextMySqlModel.java
    job --> ProjectMySqlModel.java
    job --> ProjectMemberMySqlModel.java
    chat --> ChatUnreadMessageMySqlModel.java
    chat --> MemberChatMySqlModel.java
    chat --> ChatLastAccountMysqlModel.java
    chat --> MessageQueueMySqlModel.java
    data_set --> ImageDataSetSampleMysqlModel.java
    data_set --> DataSetColumnMysqlModel.java
    flow --> FlowActionLogMySqlModel.java
    flow --> FlowTemplateMySqlModel.java
    flow --> FlowActionQueueMySqlModel.java
    fusion --> bloomfilter
    fusion --> FusionActuatorInfoMySqlModel.java
    fusion --> FusionTaskMySqlModel.java
    fusion --> FusionResultMySqlModel.java
    fusion --> FieldInfoMySqlModel.java
    fusion --> ExportProgressMySqlModel.java
    bloomfilter --> BloomFilterTaskMysqlModel.java
    bloomfilter --> BloomFilterColumnMysqlModel.java
    base --> AbstractBaseMySqlModel.java
    base --> AbstractMySqlModel.java
```

该流程图展示了WeFe项目中board-service模块的数据库相关代码结构，主要分为repository（数据访问层）和entity（实体类）两大分支。repository下包含多个子目录和直接文件，如data_resource、fusion等；entity下则按业务领域划分了cert、job、chat等子目录。整个结构层次清晰，完整呈现了数据库相关的代码组织方式。

# 文件列表

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| [entity](entity/_module.md) | package | 模块管理数字证书全生命周期，含密钥存储、申请签发。数据结构包括CertKeyInfoMysqlModel等，依赖JPA框架。支持联盟链入网认证等场景。 |
| [DataSourceConfig.java](DataSourceConfig.md) | file | 配置类DataSourceConfig继承AbstractJpaConfig，定义主数据源board及JPA相关Bean，包括实体管理工厂和事务管理器，设置命名策略。 |
| [repository](repository/_module.md) | package | Spring Data JPA实现的资源管理仓库层，统一管理各类数据资源，提供CRUD扩展功能。包含数据清理、状态维护、使用统计等业务场景，支持原生SQL和事务操作。 |


