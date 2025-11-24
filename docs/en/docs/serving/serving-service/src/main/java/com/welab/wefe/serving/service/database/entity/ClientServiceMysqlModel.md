# Basic Information

|      |      |
|------|------|
| Name | ClientServiceMysqlModel |
| Language | .java |
| Code Path | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/database/entity/ClientServiceMysqlModel.java |
| Package Name | com.welab.wefe.serving.service.database.entity |
| Dependencies | ['javax.persistence.Column', 'javax.persistence.Entity', 'javax.persistence.EnumType', 'javax.persistence.Enumerated', 'com.welab.wefe.common.constant.SecretKeyType', 'com.welab.wefe.common.fieldvalidate.annotation.Check', 'com.welab.wefe.serving.service.enums.ServiceClientTypeEnum', 'com.welab.wefe.serving.service.enums.ServiceStatusEnum'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| ClientServiceMysqlModel | class |  |



## Class ClientServiceMysqlModel

|      |      |
|------|------|
| Access Modifier | @Entity(name = "client_service");public |
| Type | class |
| Name | ClientServiceMysqlModel |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
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

### Method List

| Name  | Type  | Description |
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




