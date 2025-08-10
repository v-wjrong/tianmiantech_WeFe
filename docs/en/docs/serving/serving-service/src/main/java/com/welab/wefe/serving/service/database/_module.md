# Basic Information

|      |      |
|------|------|
| Name | database |
| Language | .java |
| Code Path | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/database |
| Package Name | docs.serving.serving-service.src.main.java.com.welab.wefe.serving.service.database |
| Brief Description | An enhanced repository layer based on Spring Data JPA, providing unified data access, audit logging, dynamic field updates, and SQL query conversion. Supports complex queries, multi-table joins, and cross-database aggregation, suitable for financial-grade data services. The data persistence layer for federated learning services implements ORM operations through JPA entity mapping, covering full lifecycle data management. Configuration classes support multi-data source environments, defining primary data sources, entity scan paths, and transaction management. |

# Description

## Overview  
This module serves as the ORM persistence layer for the federated learning service system, with its core responsibilities including multi-data source management, unified audit tracking, and complex query conversion through Spring Data JPA, akin to an enterprise-level data mid-platform. The interface specifications utilize JPA annotations to define table structures (e.g., `@Entity`/`@Column`) and dynamic SQL (e.g., `@Query`). Key data structures encompass 20+ entity classes (e.g., `PredictLogMySqlModel`) and statistical DTOs (e.g., `StatisticsSumModel`), all inheriting from the `AbstractMySqlModel` base class. Dependencies include Spring Data JPA, MySQL drivers, and encryption components (e.g., `DatabaseEncryptConverter`). For instance, `AccountRepository` implements automatic state management, while `FeeConfigMysqlModel` uses the `PayTypeEnum` enum for payment types.  

## Key Business Scenarios  
The module supports federated learning lifecycle data management, with business processes covering service invocation (`ServiceCallLogMysqlModel`), fee settlement (`FeeDetailMysqlModel`), and predictive analysis (`PredictStatisticsMySqlModel`). The interaction pattern involves: multi-data source CRUD → dynamic condition filtering → factory-injected extended functionalities (e.g., automatic pagination). Typical applications include real-time API call volume statistics (`RequestStatisticsMysqlModel`) and encrypted configuration storage (`GlobalConfigMysqlModel`). Integration cases involve PSI result storage (`PsiServiceResultMysqlModel`) and model SQL configuration (`ModelSqlConfigMySqlModel`). Full functionality spans transaction management, cross-database aggregation, and state machine control (e.g., the service activation workflow in `ClientServiceMysqlModel`).


### Package Internal Structure View

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

This flowchart illustrates the complete structure of a database module, comprising three main submodules: repository, entity, and config. The repository submodule contains numerous concrete Repository implementation classes and a base foundational package. The entity submodule includes various data model classes, while the config submodule consists of configuration classes. The overall structure is clear, reflecting a typical data access layer design pattern.

# File List

| Name   | Type  | Description |
|-------|------|-------------|
| [config](config/_module.md) | package | The configuration class DataSourceConfig extends AbstractJpaConfig, defining the primary data source "serving", entity manager factory, and transaction manager, utilizing JPA with naming strategy settings. |
| [entity](entity/_module.md) | package | FeeDetailOutputModel stores fee details; PredictLogMySqlModel records prediction logs; MessageMysqlModel manages messages; PredictStatisticsMySqlModel tracks prediction data; GlobalSettingMySqlModel stores global configurations; RequestStatisticsMysqlModel logs requests; TableServiceMySqlModel maps table services; GlobalConfigMysqlModel stores encryption settings; ClientServiceMysqlModel links to client services; PsiServiceResultMysqlModel stores PSI results; ModelSqlConfigMySqlModel holds SQL configurations; AccountMySqlModel manages accounts; FeeConfigMysqlModel configures fees; ModelPredictScoreStatisticsMySqlModel tracks prediction scores; StatisticsSumModel stores statistical data; BaseServiceMySqlModel serves as the service base class; ServiceOrderMysqlModel stores service orders; ModelPredictScoreRecordMySqlModel records prediction scores; PartnerMysqlModel stores partner information; OperationLogMysqlModel logs operational activities; VerificationCodeMysqlModel stores verification codes; ServiceCallLogMysqlModel records service calls; MemberMySqlModel stores member information; PaymentsRecordsMysqlModel stores payment records; ClientServiceOutputModel outputs client services; AbstractBaseMySqlModel serves as the abstract base class; ApiRequestRecordMysqlModel logs API requests; ClientMysqlModel stores client information; ModelMemberBaseModel associates model members; FeeDetailMysqlModel stores fee details; DataSourceMySqlModel stores data sources; TableModelMySqlModel maps table models; AbstractMySqlModel serves as the abstract parent class; ModelMemberMySqlModel associates model members; OrderStatisticsMysqlModel tracks order data. |
| [repository](repository/_module.md) | package | Multiple Spring Data JPA repository interfaces inherit from BaseRepository, providing database operations for account management, billing records, client services, and prediction statistics. They support native SQL queries, pagination filtering, and transaction management. |


