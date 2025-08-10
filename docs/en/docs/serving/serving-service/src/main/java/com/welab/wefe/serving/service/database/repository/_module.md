# Basic Information

|      |      |
|------|------|
| Name | repository |
| Language | .java |
| Code Path | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/database/repository |
| Package Name | docs.serving.serving-service.src.main.java.com.welab.wefe.serving.service.database.repository |
| Brief Description | Multiple Spring Data JPA repository interfaces inherit from BaseRepository, providing database operations for account management, billing records, client services, and prediction statistics. They support native SQL queries, pagination filtering, and transaction management. |

# Description

## Overview  
This module is an enhanced repository layer implementation based on Spring Data JPA, with its core responsibility being to provide unified data access capabilities and extended CRUD functionality. It leverages the `BaseRepository` base class and factory pattern to achieve audit tracking (e.g., automatic operation timestamp recording), dynamic field updates, and native SQL query conversion, akin to the JPA template pattern. Key data structures include generic entity models (e.g., `PredictStatisticsMySqlModel`) and statistical DTOs (e.g., `StatisticsSumModel`), relying on the Spring Data JPA core library and `EntityManager`. For instance, `AccountRepository` supports automated account status management, while `OrderStatisticsRepository` implements multi-granularity time-grouped statistics.  

## Key Business Scenarios  
It is typically applied in persistence layer scenarios requiring complex queries and unified auditing, such as account management (automatic deactivation of inactive accounts), billing statistics (multi-dimensional aggregation analysis), and prediction log analysis (grouped by model/member). The interaction pattern involves: inheriting `BaseRepository` for basic CRUD → defining native SQL via `@Query` → injecting enhanced features (e.g., automatic pagination/cache clearance) through the factory. Examples include `FeeRecordRepository` for multi-table paginated queries and `PredictScoreStatisticsRepository` for dynamic score distribution statistics. Full functionality covers transaction management, dynamic condition filtering, multi-table joins, and cross-database aggregation, making it suitable for financial-grade data service scenarios.


### Package Internal Structure View

```mermaid
graph TD
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
```

This flowchart illustrates the file structure within the repository directory of a Java project, comprising 34 file nodes and 1 subdirectory node. All Repository class files are directly subordinate to the repository directory, with the base subdirectory containing 3 foundational Repository-related files. The entire structure clearly presents the organization of the data access layer, where Repository classes are arranged flatly by functionality, while core implementation classes are centralized in the base subdirectory.

# File List

| Name   | Type  | Description |
|-------|------|-------------|
| [AccountRepository.java](AccountRepository.md) | file | The AccountRepository interface extends BaseRepository, providing functionalities to query accounts by mobile number, revoke super administrator privileges, update the last operation time, disable accounts inactive for 90 days, and delete accounts inactive for 180 days. |
| [BaseServiceRepository.java](BaseServiceRepository.md) | file | The interface BaseServiceRepository extends BaseRepository, with the generic type T required to extend BaseServiceMySqlModel, annotated with @Repository for naming. |
| [FeeRecordRepository.java](FeeRecordRepository.md) | file | The FeeRecordRepository interface extends BaseRepository, providing native SQL methods for querying fee detail lists and counting, supporting multi-condition filtering and pagination. |
| [ClientServiceQueryRepository.java](ClientServiceQueryRepository.md) | file | The ClientServiceQueryRepository interface provides customer service data query functionality, including three methods: paginated query list, total count statistics, and querying details by ID. It utilizes native SQL to implement multi-table joins and conditional filtering. |
| [FeeDetailRepository.java](FeeDetailRepository.md) | file | The FeeDetailRepository interface extends BaseRepository and is used to operate on FeeDetailMysqlModel data. It includes the native SQL query method getLastRecord, which retrieves the last record from the fee_detail table sorted by updated_time in descending order. |
| [ServiceOrderRepository.java](ServiceOrderRepository.md) | file | This is a Spring Repository interface that extends BaseRepository, designed to operate on data of type ServiceOrderMysqlModel with a primary key type of String. |
| [MemberRepository.java](MemberRepository.md) | file | The member repository interface inherits from the base repository and operates on data of type MemberMySqlModel, with the primary key being of type String. |
| [MessageRepository.java](MessageRepository.md) | file | The message repository interface inherits from the base repository, operating on the message model with a string-type primary key. |
| [DataSourceRepository.java](DataSourceRepository.md) | file | The DataSourceRepository interface extends BaseRepository and provides the countByName method for counting by name, using native SQL queries. |
| [PredictStatisticsRepository.java](PredictStatisticsRepository.md) | file | The `PredictStatisticsRepository` interface extends `BaseRepository`, providing methods to query by model ID and member ID, retrieve all member IDs and model IDs, as well as query predictive statistics grouped by day, hour, month, and minute. |
| [ModelSqlConfigRepository.java](ModelSqlConfigRepository.md) | file | The interface ModelSqlConfigRepository extends BaseRepository, operates on data of type ModelSqlConfigMySqlModel, with the primary key being String. |
| [TableModelRepository.java](TableModelRepository.md) | file | This is a Spring Data JPA repository interface that extends the base service repository, used for operating table model data. It includes a native SQL query method to retrieve a list of all service IDs with service type 7. |
| [OperationLogRepository.java](OperationLogRepository.md) | file | This is a Spring Data repository interface for operation logs, which extends the base repository class and is used for MySQL model data access of operation logs. |
| [PaymentsRecordsRepository.java](PaymentsRecordsRepository.md) | file | Payment Record Repository Interface, inherits from the base repository class, operates on the Payment Record MySQL model, with the primary key type as string. |
| [GlobalConfigRepository.java](GlobalConfigRepository.md) | file | This is a Spring Data JPA repository interface that extends the base repository and defines a query method by group. |
| [GlobalSettingRepository.java](GlobalSettingRepository.md) | file | The GlobalSettingRepository interface extends BaseRepository and implements the singleton query method singleton() via the @Query annotation, returning a GlobalSettingMySqlModel. |
| [TableServiceRepository.java](TableServiceRepository.md) | file | The interface TableServiceRepository extends BaseServiceRepository and is marked as a table service repository with the @Repository annotation. |
| [PredictLogRepository.java](PredictLogRepository.md) | file | This is a Spring repository interface that extends the base repository class, designed for operating on PredictLogMySqlModel type data with a primary key of String type. |
| [OrderStatisticsRepository.java](OrderStatisticsRepository.md) | file | The OrderStatisticsRepository interface provides order statistics functionality, including methods for retrieving the latest records and aggregating order data by minute, hour, day, and month granularities, with support for multi-criteria filtering. |
| [ModelMemberRepository.java](ModelMemberRepository.md) | file | The ModelMemberRepository interface extends BaseRepository, providing methods to query ModelMemberMySqlModel by modelId, memberId, and role. |
| [PartnerRepository.java](PartnerRepository.md) | file | Partner repository interface, inherits from the base repository, operates on PartnerMysqlModel type data with a string-type primary key. |
| [ModelPredictScoreStatisticsRepository.java](ModelPredictScoreStatisticsRepository.md) | file | The code defines a Spring Data JPA repository interface for querying model prediction score statistics. It uses native SQL to group and count by split_point, supporting filtering by service ID and time range. Returns a list of statistical results. |
| [ClientRepository.java](ClientRepository.md) | file | Client repository interface, inherits from the base repository class, operates on the ClientMysqlModel entity, with the primary key type as String. |
| [RequestStatisticsRepository.java](RequestStatisticsRepository.md) | file | The RequestStatisticsRepository interface extends BaseRepository, querying interface request statistics grouped by service ID and client ID through native SQL, including counts of successful, failed, and total requests. |
| [PredictScoreStatisticsRepository.java](PredictScoreStatisticsRepository.md) | file | Define the PredictScoreStatisticsRepository interface, extending BaseRepository, using native SQL queries to group statistics by split_point and calculate the total sum of data for a specified service ID within a given time range. |
| [ServiceCallLogRepository.java](ServiceCallLogRepository.md) | file | The interface ServiceCallLogRepository extends BaseRepository and is used to operate on ServiceCallLogMysqlModel data, with the primary key type being String. |
| [ApiRequestRecordRepository.java](ApiRequestRecordRepository.md) | file | The interface ApiRequestRecordRepository extends BaseRepository and is used to operate on ApiRequestRecordMysqlModel data, with the primary key type being String. |
| [PsiServiceResultRepository.java](PsiServiceResultRepository.md) | file | This is a Spring repository interface named PsiServiceResultRepository, which extends BaseRepository and is used to manipulate data of type PsiServiceResultMysqlModel with a primary key type of String. |
| [FeeConfigRepository.java](FeeConfigRepository.md) | file | The FeeConfigRepository interface extends BaseRepository, providing native SQL methods to update fields such as unitPrice and payType via serviceId and clientId, with support for automatic cache clearance and transaction management. |
| [ClientServiceRepository.java](ClientServiceRepository.md) | file | Client Service Repository Interface, extending the base repository, provides native SQL methods for updating status, modifier, and timestamp based on service ID and client ID. |
| [VerificationCodeRepository.java](VerificationCodeRepository.md) | file | The interface VerificationCodeRepository extends BaseRepository and is used to operate VerificationCodeMysqlModel data, with the primary key type being String. |
| [ModelMemberBaseRepository.java](ModelMemberBaseRepository.md) | file | The ModelMemberBaseRepository interface extends BaseRepository, providing native SQL methods for querying ModelMemberBaseModel lists by modelId and role. |
| [ModelPredictScoreRecordRepository.java](ModelPredictScoreRecordRepository.md) | file | This is a Spring Data repository interface that extends the base repository class, designed for operating on the `ModelPredictScoreRecordMySqlModel` entity with a primary key type of String. |
| [base](base/_module.md) | package | Implement a custom Spring Data JPA repository factory bean by extending JpaRepositoryFactoryBean to create custom repository instances. BaseRepositoryImpl provides extended CRUD functionalities, supporting field queries, batch updates, pagination, and native SQL. The BaseRepository interface is marked as NoRepositoryBean, extending JPA capabilities with transactional annotations. |


