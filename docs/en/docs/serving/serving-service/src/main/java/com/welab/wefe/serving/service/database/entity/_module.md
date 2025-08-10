# Basic Information

|      |      |
|------|------|
| Name | entity |
| Language | .java |
| Code Path | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/database/entity |
| Package Name | docs.serving.serving-service.src.main.java.com.welab.wefe.serving.service.database.entity |
| Brief Description | FeeDetailOutputModel stores fee details; PredictLogMySqlModel records prediction logs; MessageMysqlModel manages messages; PredictStatisticsMySqlModel tracks prediction data; GlobalSettingMySqlModel stores global configurations; RequestStatisticsMysqlModel logs requests; TableServiceMySqlModel maps table services; GlobalConfigMysqlModel stores encryption settings; ClientServiceMysqlModel links to client services; PsiServiceResultMysqlModel stores PSI results; ModelSqlConfigMySqlModel holds SQL configurations; AccountMySqlModel manages accounts; FeeConfigMysqlModel configures fees; ModelPredictScoreStatisticsMySqlModel tracks prediction scores; StatisticsSumModel stores statistical data; BaseServiceMySqlModel serves as the service base class; ServiceOrderMysqlModel stores service orders; ModelPredictScoreRecordMySqlModel records prediction scores; PartnerMysqlModel stores partner information; OperationLogMysqlModel logs operational activities; VerificationCodeMysqlModel stores verification codes; ServiceCallLogMysqlModel records service calls; MemberMySqlModel stores member information; PaymentsRecordsMysqlModel stores payment records; ClientServiceOutputModel outputs client services; AbstractBaseMySqlModel serves as the abstract base class; ApiRequestRecordMysqlModel logs API requests; ClientMysqlModel stores client information; ModelMemberBaseModel associates model members; FeeDetailMysqlModel stores fee details; DataSourceMySqlModel stores data sources; TableModelMySqlModel maps table models; AbstractMySqlModel serves as the abstract parent class; ModelMemberMySqlModel associates model members; OrderStatisticsMysqlModel tracks order data. |

# Description

## Overview  
This module serves as the data persistence layer of the federated learning service system, with its core responsibility being to map database table structures through JPA entity classes and implement ORM operations for business data. The interface specifications uniformly adopt JPA annotations to define table names, column mappings, and field constraints, such as @Column/@Entity annotations. Key data structures include 20+ entity classes like FeeDetailOutputModel, PredictLogMySqlModel, and GlobalSettingMySqlModel, all of which inherit from the AbstractMySqlModel base class. External dependencies primarily include the JPA specification, MySQL driver, and encryption components (e.g., DatabaseEncryptConverter). For instance, FeeConfigMysqlModel uses the PayTypeEnum enum to define payment types, while ModelPredictScoreStatisticsMySqlModel records model prediction score distributions.  

## Core Business Scenarios  
The module supports data management throughout the entire lifecycle of federated learning, akin to a data middle platform in an enterprise-level SaaS system. Business processes cover scenarios such as service invocation (ServiceCallLogMysqlModel), fee settlement (FeeDetailMysqlModel), and model prediction (PredictStatisticsMySqlModel), forming a complete data chain through entity class associations. The interaction model employs CRUD operations and state machine management—for example, ClientServiceMysqlModel uses status fields to control service activation workflows. Typical applications include real-time API call volume statistics (RequestStatisticsMysqlModel), encrypted storage of sensitive configurations (GlobalConfigMysqlModel), and asynchronous logging of operational activities (OperationLogMysqlModel). API types range from basic data services (e.g., MemberMySqlModel) to business aggregation services (e.g., OrderStatisticsMysqlModel). Integration cases include PSI service result storage (PsiServiceResultMysqlModel) and model SQL configuration management (ModelSqlConfigMySqlModel).


### Package Internal Structure View

```mermaid
graph TD
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
```

This flowchart illustrates the hierarchical relationships of database entity classes in the WeFe service project. All entity class files are located under the entity directory, comprising 34 distinct model class files that cover various business entity types such as fee details, prediction logs, message records, and statistical information. These entity classes form the core data structure foundation for interactions between the service layer and the database.

# File List

| Name   | Type  | Description |
|-------|------|-------------|
| [FeeDetailOutputModel.java](FeeDetailOutputModel.md) | file | The FeeDetailOutputModel is a JPA entity class that contains fields such as service and customer information, unit price, payment type, call count, total fee, and statistical date. |
| [PredictLogMySqlModel.java](PredictLogMySqlModel.md) | file | The `PredictLogMySqlModel` class defines the MySQL entity for prediction logs, containing fields such as ID, serial number, member ID, model ID, algorithm, federated learning type, role, creation time, request, response, time consumption, and result. |
| [MessageMysqlModel.java](MessageMysqlModel.md) | file | Message entity class, containing fields for producer type, message level, title, content, and unread status, along with their corresponding getter/setter methods. |
| [PredictStatisticsMySqlModel.java](PredictStatisticsMySqlModel.md) | file | This is a MySQL entity class named predict_statistics, containing prediction statistics such as ID, member ID, model ID, time fields (month, day, hour, minute), total count, success count, failure count, and creation/update timestamps. It provides methods for setting date fields. |
| [GlobalSettingMySqlModel.java](GlobalSettingMySqlModel.md) | file | The GlobalSettingMySqlModel is a MySQL entity class that includes member ID, name, RSA key, gateway URI, and service base URL fields along with their corresponding getter/setter methods. |
| [RequestStatisticsMysqlModel.java](RequestStatisticsMysqlModel.md) | file | MySQL Request Statistics Entity Class, containing fields such as ID, Service ID/Name, Client ID/Name, Success/Failure/Total Call Counts, and Service Type, along with corresponding getter/setter methods. |
| [TableServiceMySqlModel.java](TableServiceMySqlModel.md) | file | MySQL model class for table services, containing fields such as query parameters, data sources, and service configurations, used to store JSON-formatted configuration information and operator data. |
| [GlobalConfigMysqlModel.java](GlobalConfigMysqlModel.md) | file | GlobalConfigMysqlModel is a MySQL entity class that includes fields for configuration group, name, encrypted value, and description, providing getter/setter methods. |
| [ClientServiceMysqlModel.java](ClientServiceMysqlModel.md) | file | The ClientServiceMysqlModel class maps to the client_service table, containing fields such as service ID, client ID, name, type, status, IP, URL, price, and secret key. The default status is unused, and the secret key type is RSA. |
| [PsiServiceResultMysqlModel.java](PsiServiceResultMysqlModel.md) | file | PSI service result MySQL entity class, including ID, creation time, request ID, service ID, service name, and result fields, implementing the serializable interface. |
| [ModelSqlConfigMySqlModel.java](ModelSqlConfigMySqlModel.md) | file | The ModelSqlConfigMySqlModel class maps to the model_sql_config table, containing fields such as modelId, dataSourceId, and sqlContext, along with their corresponding getter/setter methods. |
| [AccountMySqlModel.java](AccountMySqlModel.md) | file | Account entity class, including fields such as phone number, password, nickname, and email, supports encrypted storage, distinguishes between super administrators and regular administrators, and records audit status, historical passwords, and other information. |
| [FeeConfigMysqlModel.java](FeeConfigMysqlModel.md) | file | FeeConfigMysqlModel is a database entity class containing fields such as serviceId, clientId, unitPrice, and payType, which represent the service ID, client ID, unit price, and payment type (1 for prepaid/0 for postpaid) respectively. |
| [ModelPredictScoreStatisticsMySqlModel.java](ModelPredictScoreStatisticsMySqlModel.md) | file | Java entity class ModelPredictScoreStatisticsMySqlModel, containing fields serviceId, day, splitPoint, and count, used for storing model prediction score statistics. |
| [StatisticsSumModel.java](StatisticsSumModel.md) | file | Java entity class StatisticsSumModel, containing fields id, splitPoint, and count, with getter and setter methods provided for each field. |
| [BaseServiceMySqlModel.java](BaseServiceMySqlModel.md) | file | BaseServiceMySqlModel is an entity class that inherits from AbstractBaseMySqlModel, mapping to the database table base_service. It includes fields such as service ID, name, URL, type, and status, and provides getter/setter methods along with a method to determine whether it is a model service. |
| [ServiceOrderMysqlModel.java](ServiceOrderMysqlModel.md) | file | Service Order MySQL entity class, including service ID, name, type, order type, status, and request/response partner information. |
| [ModelPredictScoreRecordMySqlModel.java](ModelPredictScoreRecordMySqlModel.md) | file | This is a JPA entity class named ModelPredictScoreRecordMySqlModel, which maps to the database table model_predict_score_record, containing the fields serviceId and score along with their getter and setter methods. |
| [PartnerMysqlModel.java](PartnerMysqlModel.md) | file | The PartnerMysqlModel class includes fields such as name, email, isUnionMember, servingBaseUrl, remark, status, code, and isMe, which are used to represent partner information. |
| [OperationLogMysqlModel.java](OperationLogMysqlModel.md) | file | The operation log entity class includes fields such as interface, IP, operator, action, result, and time consumption, used for recording system operation information. |
| [VerificationCodeMysqlModel.java](VerificationCodeMysqlModel.md) | file | This is a verification code entity class that includes fields such as business ID, mobile number, verification code, sending status, sending channel, business type, and response content, used for storing and managing verification code-related information. |
| [ServiceCallLogMysqlModel.java](ServiceCallLogMysqlModel.md) | file | MySQL service call log entity class, containing fields such as order ID, caller, service information, request/response data, status code, and time consumption. |
| [MemberMySqlModel.java](MemberMySqlModel.md) | file | Define a MySQL member entity class, including fields for member ID, name, API address, and public key, with corresponding getter and setter methods provided. |
| [PaymentsRecordsMysqlModel.java](PaymentsRecordsMysqlModel.md) | file | Payment record entity class, including fields for payment type, customer ID, customer name, amount, service ID, service name, service type, balance, and remarks. |
| [ClientServiceOutputModel.java](ClientServiceOutputModel.md) | file | The ClientServiceOutputModel class contains service and client information, including fields such as ID, name, price, status, key type, and request address, used for managing service output data. |
| [AbstractBaseMySqlModel.java](AbstractBaseMySqlModel.md) | file | The abstract base class AbstractBaseMySqlModel extends AbstractMySqlModel and includes the fields createdBy and updatedBy along with their corresponding getter/setter methods. |
| [ApiRequestRecordMysqlModel.java](ApiRequestRecordMysqlModel.md) | file | This is a MySQL entity class for API request logging, containing fields such as service ID, client ID, name, type, IP address, time consumption, and request result. |
| [ClientMysqlModel.java](ClientMysqlModel.md) | file | The `ClientMysqlModel` class represents a client entity, containing fields for name, email, IP address, public key, remarks, status, and code, with the status defaulting to normal. |
| [ModelMemberBaseModel.java](ModelMemberBaseModel.md) | file | Defined an entity class named ModelMemberBaseModel, which includes fields such as id, modelId, memberId, role, and api, along with corresponding getter and setter methods. |
| [FeeDetailMysqlModel.java](FeeDetailMysqlModel.md) | file | The FeeDetailMysqlModel class maps to the fee_detail table, containing fields such as service ID, client ID, name, type, total fee, request count, unit price, payment type, configuration ID, and IP, along with their corresponding getter/setter methods. |
| [DataSourceMySqlModel.java](DataSourceMySqlModel.md) | file | The DataSourceMySqlModel class defines a data source entity, which includes attributes such as name, database type, host, port, database name, username, and encrypted password, along with corresponding getter and setter methods. |
| [TableModelMySqlModel.java](TableModelMySqlModel.md) | file | MySQL database table model class, containing fields such as algorithm type, federated learning type, model parameters, feature source, file path, usage count, SQL script, data source ID, score distribution, and scorecard information. |
| [AbstractMySqlModel.java](AbstractMySqlModel.md) | file | The abstract class AbstractMySqlModel defines the base class for MySQL models, including fields such as ID, creation time, and update time. The ID is auto-generated and cannot be updated, with getter/setter methods provided. |
| [ModelMemberMySqlModel.java](ModelMemberMySqlModel.md) | file | This is a MySQL entity class named model_member, which includes the fields modelId, memberId, role, and status, representing the model ID, member ID, role, and status respectively, with the status defaulting to offline. |
| [OrderStatisticsMysqlModel.java](OrderStatisticsMysqlModel.md) | file | Order statistics MySQL entity class, including fields such as call count, success/failure count, time granularity, partner information, service information, and IP address. |


