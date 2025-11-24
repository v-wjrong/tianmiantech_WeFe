# 基础信息

|      |      |
|------|------|
| 名称 | ClientServiceMysqlModel |
| 编码语言 | .java |
| 代码路径 | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/database/entity/ClientServiceMysqlModel.java |
| 包名 | com.welab.wefe.serving.service.database.entity |
| 依赖项 | ['javax.persistence.Column', 'javax.persistence.Entity', 'javax.persistence.EnumType', 'javax.persistence.Enumerated', 'com.welab.wefe.common.constant.SecretKeyType', 'com.welab.wefe.common.fieldvalidate.annotation.Check', 'com.welab.wefe.serving.service.enums.ServiceClientTypeEnum', 'com.welab.wefe.serving.service.enums.ServiceStatusEnum'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| ClientServiceMysqlModel | class |  |



## 类 ClientServiceMysqlModel

|      |      |
|------|------|
| 访问范围 | @Entity(name = "client_service");public |
| 类型 | class |
| 名称 | ClientServiceMysqlModel |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| url | String |  |
| serialVersionUID = -2660433592111729597L | long |  |
| privateKey | String |  |
| unitPrice | Double |  |
| code | String |  |
| publicKey | String |  |
| ipAdd | String |  |
| clientName | String |  |
| status = ServiceStatusEnum.UNUSED.getCode() | Integer |  |
| serviceName | String |  |
| serviceType | Integer |  |
| serviceId | String |  |
| type = ServiceClientTypeEnum.OPEN.getValue() | Integer |  |
| clientId | String |  |
| secretKeyType = SecretKeyType.rsa | SecretKeyType |  |
| payType | Integer |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| setType | void |  |
| setCode | void |  |
| getUrl | String |  |
| setUnitPrice | void |  |
| setPayType | void |  |
| getUnitPrice | Double |  |
| getClientId | String |  |
| setServiceType | void |  |
| setPrivateKey | void |  |
| setPublicKey | void |  |
| getServiceType | Integer |  |
| getIpAdd | String |  |
| getCode | String |  |
| setIpAdd | void |  |
| setServiceName | void |  |
| setUrl | void |  |
| setServiceId | void |  |
| getServiceId | String |  |
| getPayType | Integer |  |
| getServiceName | String |  |
| getType | Integer |  |
| setClientName | void |  |
| setStatus | void |  |
| getStatus | Integer |  |
| getClientName | String |  |
| getPrivateKey | String |  |
| getPublicKey | String |  |
| setClientId | void |  |
| getSecretKeyType | SecretKeyType |  |
| setSecretKeyType | void |  |




