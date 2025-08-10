# 基础信息

|      |      |
|------|------|
| 名称 | serving-service |
| 编码语言 | .java |
| 代码路径 | WeFe/serving/serving-service |
| 包名 | docs.serving.serving-service |
| 概述说明 | Java隐私计算客户端模块，支持RSA/SM2签名、HTTP POST和JSON，实现匿踪查询、集合求交和安全预测。联邦学习核心组件，微服务架构，管理配置、预测、持久化和安全通信，支撑系统初始化、联合预测和服务治理全流程。 |

# 说明

## 概述  
该模块是融合隐私计算与联邦学习能力的复合型系统，核心职责为安全数据交互（类似加密网关模式）和分布式机器学习协同（类似主从架构）。接口规范分层设计：基础层采用RSA/SM2签名和JSON格式（如PirClient），服务层遵循RESTful标准和模板方法模式（如AbstractApi）。关键数据结构聚合为五类：密钥配置（客户密钥对/SM2密钥）、计算参数（FederatedPredictParam/查询参数）、系统配置（PSI批量大小/服务地址）、持久化模型（PredictLogMySqlModel）和状态枚举（ServiceTypeEnum）。外部依赖包含加密库（RSA/SM2）、Spring生态（JPA/Cloud）、多数据库驱动（MySQL/Doris/Hive）及HTTP组件。例如PirClient处理匿踪查询，PromoterPredictor协调多方预测。

## 主要业务场景  
模块支撑隐私计算与联邦学习的全链路场景，业务流程整合为：1) 安全初始化（密钥生成→配置加载→服务注册）；2) 联合计算（特征签名→多方PSI→模型预测→结果聚合）；3) 治理闭环（日志记录→费用结算）。典型交互采用混合模式：隐私计算类似API网关（统一签名验证），联邦学习类似主从架构（PromoterPredictor协调）。功能完整性体现在加密通信（SM2/RSA）、成员管理（member_id）、预测引擎（Predicter）和持久化（Database）的协同。例如金融场景中，MultiPsi实现银行间数据比对→ModelPredictClient发起安全预测→记录PredictLogMySqlModel。API覆盖初始化、预测、定时任务三类，集成案例可见于ServingService启动流程（加载处理器→初始化监听器→启动API服务）。


### 包内部结构视图

None

# 文件列表

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| [com](src/main/java/com/_module.md) | folder | Config类：Spring组件，加载外部配置，定义文件路径、邮件主题等属性，支持UTF-8编码。XxxModelProcessor类：继承抽象类，空实现预处理和后处理方法。联邦学习核心API：提供加密通信、成员管理等功能，RESTful设计。预测引擎：支持联合预测，含标准、批量、调试模式。ORM层：JPA实现数据管理，含20+实体类。工具集：签名验证、加密等。枚举模块：定义服务状态和类型。隐私计算框架：处理PSI/PIR/SA请求。特征管理：统一管理数据源和模型。服务治理：全局配置和模型生命周期管理。定时任务：执行统计和状态维护。DTO管理：封装业务数据交互。日志处理：记录API日志到MySQL。启动监听器：执行初始化任务。特征处理框架：注解和SQL驱动。ServingService主类：Spring Boot应用启动配置。 |


