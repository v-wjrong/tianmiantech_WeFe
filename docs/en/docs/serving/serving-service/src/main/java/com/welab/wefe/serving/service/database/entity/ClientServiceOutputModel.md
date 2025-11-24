# Basic Information

|      |      |
|------|------|
| Name | ClientServiceOutputModel |
| Language | .java |
| Code Path | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/database/entity/ClientServiceOutputModel.java |
| Package Name | com.welab.wefe.serving.service.database.entity |
| Dependencies | ['com.welab.wefe.common.constant.SecretKeyType', 'javax.persistence', 'java.util.UUID'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| ClientServiceOutputModel | class |  |



## Class ClientServiceOutputModel

|      |      |
|------|------|
| Access Modifier | @Entity;public |
| Type | class |
| Name | ClientServiceOutputModel |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
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

### Method List

| Name  | Type  | Description |
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




