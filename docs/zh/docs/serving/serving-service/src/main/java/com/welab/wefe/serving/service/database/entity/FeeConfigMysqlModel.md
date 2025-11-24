# 基础信息

|      |      |
|------|------|
| 名称 | FeeConfigMysqlModel |
| 编码语言 | .java |
| 代码路径 | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/database/entity/FeeConfigMysqlModel.java |
| 包名 | com.welab.wefe.serving.service.database.entity |
| 依赖项 | ['com.welab.wefe.serving.service.enums.PayTypeEnum', 'javax.persistence.Column', 'javax.persistence.Entity'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| FeeConfigMysqlModel | class |  |



## 类 FeeConfigMysqlModel

|      |      |
|------|------|
| 访问范围 | @Entity(name = "fee_config");public |
| 类型 | class |
| 名称 | FeeConfigMysqlModel |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| clientId | String |  |
| payType = PayTypeEnum.POSTPAID.getCode() | int |  |
| serviceId | String |  |
| unitPrice | Double |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| setClientId | void |  |
| getUnitPrice | Double |  |
| setServiceId | void |  |
| getClientId | String |  |
| getServiceId | String |  |
| setUnitPrice | void |  |
| getPayType | int |  |
| setPayType | void |  |




