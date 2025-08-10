# 基础信息

|      |      |
|------|------|
| 名称 | serving |
| 编码语言 | .java |
| 代码路径 | WeFe/serving |
| 包名 | docs.serving |
| 概述说明 | 联邦学习预测框架统一管理预测流程与结果合并，支持横向/纵向联邦，依赖XGBoost和多线程工具。隐私计算系统整合安全数据交互与机器学习协同，采用分层设计，支持加密通信与联合计算，依赖加密库和Spring生态。 |

# 说明

## 概述  
该模块是融合联邦学习与隐私计算的协同系统，核心职责为安全数据交互（类似加密网关）和分布式预测流程管理（类似主从架构）。通过分层接口设计（基础层RSA/SM2签名与服务层RESTful API）和模板方法模式（如AbstractAlgorithm/AbstractApi）实现标准化。关键数据结构包括五类：密钥配置（SM2密钥对）、计算参数（FederatedPredictParam）、模型对象（LrPredictResultModel）、系统配置（PSI批量大小）和状态枚举（ServiceTypeEnum）。外部依赖涉及加密库（SM2/RSA）、机器学习框架（XGBoost）、多数据库驱动（MySQL/Doris）及联邦组件（WeFe）。例如PirClient处理匿踪查询，AlgorithmManager动态加载预测算法。

## 主要业务场景  
模块支持联邦预测与隐私计算全链路，典型流程为：1) 安全初始化（密钥生成→服务注册）；2) 联合计算（PSI对齐→模型预测→结果聚合）；3) 治理闭环（日志记录→费用结算）。交互模式混合API网关（统一签名验证）与主从架构（PromoterPredictor协调），功能完整性体现在加密通信（SM2）、多算法支持（XGBoost树合并/逻辑回归分箱）及状态管理（StateCode）。例如金融场景中MultiPsi完成银行数据比对→XgboostVertPromoterAlgorithm合并远程预测结果→记录PredictLogMySqlModel。API覆盖初始化、批量预测、定时任务三类，集成案例可见于ServingService启动流程（加载处理器→监听器初始化→API服务暴露）。


### 包内部结构视图

None

# 文件列表

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| [serving-sdk-java](serving-sdk-java/src/main/java/com/_module.md) | module | 该模块提供联邦学习预测框架，支持逻辑回归和XGBoost算法，涵盖单条/批量处理、参数校验、结果合并。通过抽象类和模板方法定义标准化流程，依赖注解和反射实现动态加载。关键组件包括模型处理器、算法管理器和线程池，适用于实时和离线预测场景。 |
| [serving-service](serving-service/src/main/java/com/_module.md) | module | Java隐私计算客户端模块，支持RSA/SM2签名、HTTP POST和JSON，实现匿踪查询、集合求交和安全预测。联邦学习核心组件，微服务架构，管理配置、预测、持久化和安全通信，支撑系统初始化、联合预测和服务治理全流程。 |


