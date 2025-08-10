# 基础信息

|      |      |
|------|------|
| 名称 | database |
| 编码语言 | .java |
| 代码路径 | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/database |
| 包名 | docs.serving.serving-service.src.main.java.com.welab.wefe.serving.service.database |
| 概述说明 | 基于Spring Data JPA的增强仓储层，提供统一数据访问、审计追踪、动态字段更新及SQL查询转换。支持复杂查询、多表关联和跨库聚合，适用于金融级数据服务。联邦学习服务的数据持久化层，通过JPA实体映射实现ORM操作，涵盖全生命周期数据管理。配置类支持多数据源环境，定义主数据源、实体扫描路径和事务管理。 |

# 说明

## 概述  
该模块是联邦学习服务系统的ORM持久化层，核心职责是通过Spring Data JPA实现多数据源管理、统一审计追踪和复杂查询转换，类似企业级数据中台。接口规范采用JPA注解定义表结构（如@Entity/@Column）和动态SQL（如@Query），关键数据结构包括20+实体类（如PredictLogMySqlModel）和统计DTO（如StatisticsSumModel），均继承AbstractMySqlModel基类。依赖项包括Spring Data JPA、MySQL驱动和加密组件（如DatabaseEncryptConverter）。例如AccountRepository实现自动状态管理，FeeConfigMysqlModel使用PayTypeEnum枚举支付类型。

## 主要业务场景  
模块支撑联邦学习全生命周期数据管理，业务流程涵盖服务调用（ServiceCallLogMysqlModel）、费用结算（FeeDetailMysqlModel）和预测分析（PredictStatisticsMySqlModel）。交互模式为：多数据源CRUD→动态条件筛选→工厂注入扩展功能（如自动分页）。典型应用包括实时统计API调用量（RequestStatisticsMysqlModel）、加密存储配置（GlobalConfigMysqlModel），集成案例涉及PSI结果存储（PsiServiceResultMysqlModel）和模型SQL配置（ModelSqlConfigMySqlModel）。完整功能覆盖事务管理、跨库聚合及状态机控制（如ClientServiceMysqlModel服务开通流程）。


### 包内部结构视图

```mermaid
graph TD
    database --> repository
    database --> entity
    database --> config
    repository --> AccountRepository.java
    repository --> BaseServiceRepository.java
    repository --> FeeRecordRepository.java
    repository --> ClientServiceQueryRepository.java
    repository --> FeeDetailRepository.java
    repository --> ServiceOrderRepository.java
    repository --> base
    repository --> MemberRepository.java
    repository --> MessageRepository.java
    repository --> DataSourceRepository.java
    repository --> PredictStatisticsRepository.java
    repository --> ModelSqlConfigRepository.java
    repository --> TableModelRepository.java
    repository --> OperationLogRepository.java
    repository --> PaymentsRecordsRepository.java
    repository --> GlobalConfigRepository.java
    repository --> GlobalSettingRepository.java
    repository --> TableServiceRepository.java
    repository --> PredictLogRepository.java
    repository --> OrderStatisticsRepository.java
    repository --> ModelMemberRepository.java
    repository --> PartnerRepository.java
    repository --> ModelPredictScoreStatisticsRepository.java
    repository --> ClientRepository.java
    repository --> RequestStatisticsRepository.java
    repository --> PredictScoreStatisticsRepository.java
    repository --> ServiceCallLogRepository.java
    repository --> ApiRequestRecordRepository.java
    repository --> PsiServiceResultRepository.java
    repository --> FeeConfigRepository.java
    repository --> ClientServiceRepository.java
    repository --> VerificationCodeRepository.java
    repository --> ModelMemberBaseRepository.java
    repository --> ModelPredictScoreRecordRepository.java
    base --> BaseRepositoryFactoryBean.java
    base --> BaseRepositoryImpl.java
    base --> BaseRepository.java
    entity --> FeeDetailOutputModel.java
    entity --> PredictLogMySqlModel.java
    entity --> MessageMysqlModel.java
    entity --> PredictStatisticsMySqlModel.java
    entity --> GlobalSettingMySqlModel.java
    entity --> RequestStatisticsMysqlModel.java
    entity --> TableServiceMySqlModel.java
    entity --> GlobalConfigMysqlModel.java
    entity --> ClientServiceMysqlModel.java
    entity --> PsiServiceResultMysqlModel.java
    entity --> ModelSqlConfigMySqlModel.java
    entity --> AccountMySqlModel.java
    entity --> FeeConfigMysqlModel.java
    entity --> ModelPredictScoreStatisticsMySqlModel.java
    entity --> StatisticsSumModel.java
    entity --> BaseServiceMySqlModel.java
    entity --> ServiceOrderMysqlModel.java
    entity --> ModelPredictScoreRecordMySqlModel.java
    entity --> PartnerMysqlModel.java
    entity --> OperationLogMysqlModel.java
    entity --> VerificationCodeMysqlModel.java
    entity --> ServiceCallLogMysqlModel.java
    entity --> MemberMySqlModel.java
    entity --> PaymentsRecordsMysqlModel.java
    entity --> ClientServiceOutputModel.java
    entity --> AbstractBaseMySqlModel.java
    entity --> ApiRequestRecordMysqlModel.java
    entity --> ClientMysqlModel.java
    entity --> ModelMemberBaseModel.java
    entity --> FeeDetailMysqlModel.java
    entity --> DataSourceMySqlModel.java
    entity --> TableModelMySqlModel.java
    entity --> AbstractMySqlModel.java
    entity --> ModelMemberMySqlModel.java
    entity --> OrderStatisticsMysqlModel.java
    config --> DataSourceConfig.java
```

该流程图展示了一个数据库模块的完整结构，包含repository、entity和config三个主要子模块。repository下包含大量具体的Repository实现类和base基础包，entity包含各种数据模型类，config包含配置类。整体结构清晰，体现了典型的数据访问层设计模式。

# 文件列表

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| [config](config/_module.md) | package | 配置类DataSourceConfig继承AbstractJpaConfig，定义主数据源"serving"、实体管理器工厂和事务管理器，使用JPA并设置命名策略。 |
| [entity](entity/_module.md) | package | FeeDetailOutputModel存储费用明细；PredictLogMySqlModel记录预测日志；MessageMysqlModel管理消息；PredictStatisticsMySqlModel统计预测数据；GlobalSettingMySqlModel存全局配置；RequestStatisticsMysqlModel统计请求；TableServiceMySqlModel映射表服务；GlobalConfigMysqlModel存加密配置；ClientServiceMysqlModel关联客户服务；PsiServiceResultMysqlModel存PSI结果；ModelSqlConfigMySqlModel存SQL配置；AccountMySqlModel管理账户；FeeConfigMysqlModel配置费用；ModelPredictScoreStatisticsMySqlModel统计预测分数；StatisticsSumModel存统计数据；BaseServiceMySqlModel为服务基类；ServiceOrderMysqlModel存服务订单；ModelPredictScoreRecordMySqlModel记录预测分数；PartnerMysqlModel存伙伴信息；OperationLogMysqlModel记录操作日志；VerificationCodeMysqlModel存验证码；ServiceCallLogMysqlModel记录服务调用；MemberMySqlModel存会员信息；PaymentsRecordsMysqlModel存支付记录；ClientServiceOutputModel输出客户服务；AbstractBaseMySqlModel为抽象基类；ApiRequestRecordMysqlModel记录API请求；ClientMysqlModel存客户信息；ModelMemberBaseModel关联模型成员；FeeDetailMysqlModel存费用详情；DataSourceMySqlModel存数据源；TableModelMySqlModel映射表模型；AbstractMySqlModel为抽象父类；ModelMemberMySqlModel关联模型成员；OrderStatisticsMysqlModel统计订单数据。 |
| [repository](repository/_module.md) | package | 多个Spring Data JPA仓库接口，继承BaseRepository，提供账户管理、计费记录、客户端服务、预测统计等数据库操作，支持原生SQL查询、分页筛选和事务管理。 |


