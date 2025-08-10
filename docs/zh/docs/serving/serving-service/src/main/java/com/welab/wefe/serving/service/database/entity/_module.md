# 基础信息

|      |      |
|------|------|
| 名称 | entity |
| 编码语言 | .java |
| 代码路径 | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/database/entity |
| 包名 | docs.serving.serving-service.src.main.java.com.welab.wefe.serving.service.database.entity |
| 概述说明 | FeeDetailOutputModel存储费用明细；PredictLogMySqlModel记录预测日志；MessageMysqlModel管理消息；PredictStatisticsMySqlModel统计预测数据；GlobalSettingMySqlModel存全局配置；RequestStatisticsMysqlModel统计请求；TableServiceMySqlModel映射表服务；GlobalConfigMysqlModel存加密配置；ClientServiceMysqlModel关联客户服务；PsiServiceResultMysqlModel存PSI结果；ModelSqlConfigMySqlModel存SQL配置；AccountMySqlModel管理账户；FeeConfigMysqlModel配置费用；ModelPredictScoreStatisticsMySqlModel统计预测分数；StatisticsSumModel存统计数据；BaseServiceMySqlModel为服务基类；ServiceOrderMysqlModel存服务订单；ModelPredictScoreRecordMySqlModel记录预测分数；PartnerMysqlModel存伙伴信息；OperationLogMysqlModel记录操作日志；VerificationCodeMysqlModel存验证码；ServiceCallLogMysqlModel记录服务调用；MemberMySqlModel存会员信息；PaymentsRecordsMysqlModel存支付记录；ClientServiceOutputModel输出客户服务；AbstractBaseMySqlModel为抽象基类；ApiRequestRecordMysqlModel记录API请求；ClientMysqlModel存客户信息；ModelMemberBaseModel关联模型成员；FeeDetailMysqlModel存费用详情；DataSourceMySqlModel存数据源；TableModelMySqlModel映射表模型；AbstractMySqlModel为抽象父类；ModelMemberMySqlModel关联模型成员；OrderStatisticsMysqlModel统计订单数据。 |

# 说明

## 概述  
该模块是联邦学习服务系统的数据持久化层，核心职责是通过JPA实体类映射数据库表结构，实现业务数据的ORM操作。接口规范统一采用JPA注解定义表名、列名映射和字段约束，例如@Column/@Entity注解。关键数据结构包括费用明细(FeeDetailOutputModel)、预测日志(PredictLogMySqlModel)、全局配置(GlobalSettingMySqlModel)等20+实体类，均继承自AbstractMySqlModel基类。外部依赖主要为JPA规范、MySQL驱动和加密组件（如DatabaseEncryptConverter）。例如FeeConfigMysqlModel使用枚举PayTypeEnum定义支付类型，ModelPredictScoreStatisticsMySqlModel记录模型预测分数分布。

## 主要业务场景  
模块支持联邦学习全生命周期数据管理，类似企业级SaaS平台的数据中台。业务流程涵盖服务调用（ServiceCallLogMysqlModel）、费用结算（FeeDetailMysqlModel）、模型预测（PredictStatisticsMySqlModel）等场景，通过实体类关联形成完整数据链路。交互模式采用CRUD操作与状态机管理，例如ClientServiceMysqlModel用状态字段控制服务开通流程。典型应用包括：实时统计API调用量（RequestStatisticsMysqlModel）、加密存储敏感配置（GlobalConfigMysqlModel）、异步记录操作日志（OperationLogMysqlModel）。API类型涵盖基础数据服务（如MemberMySqlModel）和业务聚合服务（如OrderStatisticsMysqlModel），集成案例包括PSI服务结果存储（PsiServiceResultMysqlModel）和模型SQL配置管理（ModelSqlConfigMySqlModel）。


### 包内部结构视图

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

该流程图展示了WeFe服务项目中数据库实体类的层级关系。所有实体类文件都位于entity目录下，包含34个不同的模型类文件，涵盖了费用明细、预测日志、消息记录、统计信息等多种业务实体类型。这些实体类构成了服务层与数据库交互的核心数据结构基础。

# 文件列表

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| [FeeDetailOutputModel.java](FeeDetailOutputModel.md) | file | FeeDetailOutputModel是JPA实体类，包含服务与客户信息、单价、付费类型、调用次数、总费用及统计日期等字段。 |
| [PredictLogMySqlModel.java](PredictLogMySqlModel.md) | file | PredictLogMySqlModel类定义了预测日志的MySQL实体，包含ID、序列号、成员ID、模型ID、算法、联邦学习类型、角色、创建时间、请求、响应、耗时和结果等字段。 |
| [MessageMysqlModel.java](MessageMysqlModel.md) | file | 消息实体类，包含生产者类型、消息级别、标题、内容和未读状态字段及其getter/setter方法。 |
| [PredictStatisticsMySqlModel.java](PredictStatisticsMySqlModel.md) | file | 这是一个名为predict_statistics的MySQL实体类，包含预测统计信息，如ID、成员ID、模型ID、时间字段（月、日、时、分）、总数、成功数、失败数及创建更新时间。提供设置日期字段的方法。 |
| [GlobalSettingMySqlModel.java](GlobalSettingMySqlModel.md) | file | GlobalSettingMySqlModel是MySQL实体类，包含成员ID、名称、RSA密钥、网关URI和服务基础URL字段及其getter/setter方法。 |
| [RequestStatisticsMysqlModel.java](RequestStatisticsMysqlModel.md) | file | MySQL请求统计实体类，包含ID、服务ID/名称、客户ID/名称、成功/失败/总调用次数和服务类型等字段及对应getter/setter方法。 |
| [TableServiceMySqlModel.java](TableServiceMySqlModel.md) | file | 表服务MySQL模型类，包含查询参数、数据源、服务配置等字段，用于存储JSON格式的配置信息及操作者等数据。 |
| [GlobalConfigMysqlModel.java](GlobalConfigMysqlModel.md) | file | GlobalConfigMysqlModel是MySQL实体类，包含配置组、名称、加密值和说明字段，提供getter/setter方法。 |
| [ClientServiceMysqlModel.java](ClientServiceMysqlModel.md) | file | ClientServiceMysqlModel类映射client_service表，包含服务ID、客户ID、名称、类型、状态、IP、URL、价格、密钥等字段，默认状态未使用，密钥类型为rsa。 |
| [PsiServiceResultMysqlModel.java](PsiServiceResultMysqlModel.md) | file | PSI服务结果MySQL实体类，包含ID、创建时间、请求ID、服务ID、服务名称和结果字段，实现序列化接口。 |
| [ModelSqlConfigMySqlModel.java](ModelSqlConfigMySqlModel.md) | file | ModelSqlConfigMySqlModel类映射model_sql_config表，包含modelId、dataSourceId和sqlContext字段及其getter/setter方法。 |
| [AccountMySqlModel.java](AccountMySqlModel.md) | file | 账户实体类，包含电话、密码、昵称、邮箱等字段，支持加密存储，区分超级管理员和普通管理员，记录审核状态、历史密码等信息。 |
| [FeeConfigMysqlModel.java](FeeConfigMysqlModel.md) | file | FeeConfigMysqlModel是数据库实体类，包含serviceId、clientId、unitPrice和payType字段，分别表示服务ID、客户ID、单价和付费类型（1预付费/0后付费）。 |
| [ModelPredictScoreStatisticsMySqlModel.java](ModelPredictScoreStatisticsMySqlModel.md) | file | Java实体类ModelPredictScoreStatisticsMySqlModel，包含serviceId、day、splitPoint和count字段，用于存储模型预测分数统计数据。 |
| [StatisticsSumModel.java](StatisticsSumModel.md) | file | Java实体类StatisticsSumModel，包含id、splitPoint和count字段，提供各字段的getter和setter方法。 |
| [BaseServiceMySqlModel.java](BaseServiceMySqlModel.md) | file | BaseServiceMySqlModel是继承AbstractBaseMySqlModel的实体类，映射数据库表base_service，包含服务ID、名称、URL、类型和状态等字段，提供getter/setter方法及判断是否为模型服务的方法。 |
| [ServiceOrderMysqlModel.java](ServiceOrderMysqlModel.md) | file | 服务订单MySQL实体类，包含服务ID、名称、类型、订单类型、状态及请求/响应合作伙伴信息。 |
| [ModelPredictScoreRecordMySqlModel.java](ModelPredictScoreRecordMySqlModel.md) | file | 这是一个名为ModelPredictScoreRecordMySqlModel的JPA实体类，映射到数据库表model_predict_score_record，包含serviceId和score两个字段及其getter和setter方法。 |
| [PartnerMysqlModel.java](PartnerMysqlModel.md) | file | PartnerMysqlModel类，包含name、email、isUnionMember、servingBaseUrl、remark、status、code、isMe字段，用于表示合作伙伴信息。 |
| [OperationLogMysqlModel.java](OperationLogMysqlModel.md) | file | 操作日志实体类，包含接口、IP、操作人、行为、结果、耗时等字段，用于记录系统操作信息。 |
| [VerificationCodeMysqlModel.java](VerificationCodeMysqlModel.md) | file | 这是一个验证码实体类，包含业务ID、手机号、验证码、发送状态、发送渠道、业务类型和响应内容等字段，用于存储和管理验证码相关信息。 |
| [ServiceCallLogMysqlModel.java](ServiceCallLogMysqlModel.md) | file | MySQL服务调用日志实体类，包含订单ID、调用方、服务信息、请求响应数据、状态码、耗时等字段。 |
| [MemberMySqlModel.java](MemberMySqlModel.md) | file | 定义MySQL成员实体类，包含成员ID、名称、API地址和公钥字段，提供对应getter和setter方法。 |
| [PaymentsRecordsMysqlModel.java](PaymentsRecordsMysqlModel.md) | file | 支付记录实体类，包含支付类型、客户ID、客户名称、金额、服务ID、服务名称、服务类型、余额和备注字段。 |
| [ClientServiceOutputModel.java](ClientServiceOutputModel.md) | file | ClientServiceOutputModel类包含服务与客户信息，如ID、名称、价格、状态、密钥类型及请求地址等字段，用于管理服务输出数据。 |
| [AbstractBaseMySqlModel.java](AbstractBaseMySqlModel.md) | file | 抽象基类AbstractBaseMySqlModel继承AbstractMySqlModel，包含createdBy和updatedBy字段及其getter/setter方法。 |
| [ApiRequestRecordMysqlModel.java](ApiRequestRecordMysqlModel.md) | file | 这是一个API请求记录的MySQL实体类，包含服务ID、客户ID、名称、类型、IP地址、耗时和请求结果等字段。 |
| [ClientMysqlModel.java](ClientMysqlModel.md) | file | ClientMysqlModel类表示客户端实体，包含名称、邮箱、IP地址、公钥、备注、状态和代码字段，状态默认为正常。 |
| [ModelMemberBaseModel.java](ModelMemberBaseModel.md) | file | 定义了一个名为ModelMemberBaseModel的实体类，包含id、modelId、memberId、role和api字段，并提供了对应的getter和setter方法。 |
| [FeeDetailMysqlModel.java](FeeDetailMysqlModel.md) | file | FeeDetailMysqlModel类映射fee_detail表，包含服务ID、客户ID、名称、类型、总费用、请求次数、单价、付费类型、配置ID和IP等字段及getter/setter方法。 |
| [DataSourceMySqlModel.java](DataSourceMySqlModel.md) | file | DataSourceMySqlModel类定义了数据源实体，包含名称、数据库类型、主机、端口、数据库名、用户名和加密密码等属性，并提供了相应的getter和setter方法。 |
| [TableModelMySqlModel.java](TableModelMySqlModel.md) | file | MySQL数据库表模型类，包含算法类型、联邦学习类型、模型参数、特征源、文件路径、使用计数、SQL脚本、数据源ID、分数分布和评分卡信息等字段。 |
| [AbstractMySqlModel.java](AbstractMySqlModel.md) | file | 抽象类AbstractMySqlModel定义MySQL模型基类，包含ID、创建时间和更新时间字段，ID自动生成不可更新，提供getter/setter方法。 |
| [ModelMemberMySqlModel.java](ModelMemberMySqlModel.md) | file | 这是一个名为model_member的MySQL实体类，包含modelId、memberId、role和status字段，分别表示模型ID、成员ID、角色和状态，其中状态默认为offline。 |
| [OrderStatisticsMysqlModel.java](OrderStatisticsMysqlModel.md) | file | 订单统计MySQL实体类，包含调用次数、成功失败次数、时间粒度、合作方信息、服务信息和IP地址等字段。 |


