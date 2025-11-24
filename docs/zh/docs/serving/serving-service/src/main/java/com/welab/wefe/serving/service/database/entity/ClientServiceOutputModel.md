# 基础信息

|      |      |
|------|------|
| 名称 | ClientServiceOutputModel |
| 编码语言 | .java |
| 代码路径 | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/database/entity/ClientServiceOutputModel.java |
| 包名 | com.welab.wefe.serving.service.database.entity |
| 依赖项 | ['com.welab.wefe.common.constant.SecretKeyType', 'javax.persistence', 'java.util.UUID'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| ClientServiceOutputModel | class |  |



## 类 ClientServiceOutputModel

|      |      |
|------|------|
| 访问范围 | @Entity;public |
| 类型 | class |
| 名称 | ClientServiceOutputModel |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| id = UUID.randomUUID().toString().replaceAll("-", "") | String |  |
| url | String |  |
| unitPrice | Double |  |
| serviceType | Integer |  |
| ipAdd | String |  |
| serviceName | String |  |
| publicKey | String |  |
| privateKey | String |  |
| clientName | String |  |
| serviceId | String |  |
| code | String |  |
| status | Integer |  |
| clientId | String |  |
| secretKeyType = SecretKeyType.rsa | SecretKeyType |  |
| payType | Integer |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| setId | void |  |
| setStatus | void |  |
| setPrivateKey | void |  |
| setClientName | void |  |
| setClientId | void |  |
| getPublicKey | String |  |
| getPayType | Integer |  |
| setPayType | void |  |
| getCode | String |  |
| getId | String |  |
| setUnitPrice | void |  |
| getUnitPrice | Double |  |
| getUrl | String |  |
| getServiceName | String |  |
| getClientId | String |  |
| setPublicKey | void |  |
| getIpAdd | String |  |
| setServiceType | void |  |
| setUrl | void |  |
| getServiceId | String |  |
| setServiceName | void |  |
| getClientName | String |  |
| getSecretKeyType | SecretKeyType |  |
| setCode | void |  |
| setIpAdd | void |  |
| getServiceType | Integer |  |
| getPrivateKey | String |  |
| setServiceId | void |  |
| getStatus | Integer |  |
| setSecretKeyType | void |  |




