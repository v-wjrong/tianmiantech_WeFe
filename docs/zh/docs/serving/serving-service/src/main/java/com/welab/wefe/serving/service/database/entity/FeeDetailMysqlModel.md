# 基础信息

|      |      |
|------|------|
| 名称 | FeeDetailMysqlModel |
| 编码语言 | .java |
| 代码路径 | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/database/entity/FeeDetailMysqlModel.java |
| 包名 | com.welab.wefe.serving.service.database.entity |
| 依赖项 | ['javax.persistence.Column', 'javax.persistence.Entity', 'java.math.BigDecimal'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| FeeDetailMysqlModel | class |  |



## 类 FeeDetailMysqlModel

|      |      |
|------|------|
| 访问范围 | @Entity(name = "fee_detail");public |
| 类型 | class |
| 名称 | FeeDetailMysqlModel |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| serviceType | Integer |  |
| serviceName | String |  |
| clientId | String |  |
| serviceId | String |  |
| feeConfigId | String |  |
| unitPrice | Double |  |
| clientName | String |  |
| totalRequestTimes | Long |  |
| totalFee | BigDecimal |  |
| saveIp | String |  |
| payType | Integer |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getFeeConfigId | String |  |
| setPayType | void |  |
| setClientName | void |  |
| getServiceType | Integer |  |
| getPayType | Integer |  |
| getSaveIp | String |  |
| setServiceId | void |  |
| setServiceName | void |  |
| setSaveIp | void |  |
| getClientId | String |  |
| setClientId | void |  |
| getTotalFee | BigDecimal |  |
| setTotalFee | void |  |
| getTotalRequestTimes | Long |  |
| setTotalRequestTimes | void |  |
| setUnitPrice | void |  |
| getServiceId | String |  |
| setServiceType | void |  |
| getUnitPrice | Double |  |
| getClientName | String |  |
| getServiceName | String |  |
| setFeeConfigId | void |  |




