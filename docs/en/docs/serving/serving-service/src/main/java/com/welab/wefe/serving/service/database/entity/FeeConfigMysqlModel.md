# Basic Information

|      |      |
|------|------|
| Name | FeeConfigMysqlModel |
| Language | .java |
| Code Path | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/database/entity/FeeConfigMysqlModel.java |
| Package Name | com.welab.wefe.serving.service.database.entity |
| Dependencies | ['com.welab.wefe.serving.service.enums.PayTypeEnum', 'javax.persistence.Column', 'javax.persistence.Entity'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| FeeConfigMysqlModel | class |  |



## Class FeeConfigMysqlModel

|      |      |
|------|------|
| Access Modifier | @Entity(name = "fee_config");public |
| Type | class |
| Name | FeeConfigMysqlModel |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| clientId | String |  |
| payType = PayTypeEnum.POSTPAID.getCode() | int |  |
| serviceId | String |  |
| unitPrice | Double |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| setClientId | void |  |
| getUnitPrice | Double |  |
| setServiceId | void |  |
| getClientId | String |  |
| getServiceId | String |  |
| setUnitPrice | void |  |
| getPayType | int |  |
| setPayType | void |  |




