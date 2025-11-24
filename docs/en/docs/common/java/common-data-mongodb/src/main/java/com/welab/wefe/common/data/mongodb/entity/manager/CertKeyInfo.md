# Basic Information

|      |      |
|------|------|
| Name | CertKeyInfo |
| Language | .java |
| Code Path | WeFe/common/java/common-data-mongodb/src/main/java/com/welab/wefe/common/data/mongodb/entity/manager/CertKeyInfo.java |
| Package Name | com.welab.wefe.common.data.mongodb.entity.manager |
| Dependencies | ['java.util.UUID', 'org.springframework.data.mongodb.core.mapping.Document', 'com.welab.wefe.common.data.mongodb.constant.MongodbTable', 'com.welab.wefe.common.data.mongodb.entity.base.AbstractNormalMongoModel', 'com.welab.wefe.common.exception.StatusCodeWithException'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| CertKeyInfo | class |  |



## Class CertKeyInfo

|      |      |
|------|------|
| Access Modifier | @Document(collection = MongodbTable.CERT_KEY_INFO);public |
| Type | class |
| Name | CertKeyInfo |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| userId | String |  |
| keyAlg | String |  |
| pkId = UUID.randomUUID().toString().replaceAll("-", "") | String |  |
| serialVersionUID = -7731011364389900165L | long |  |
| createdBy | String |  |
| keyPem | String |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getUserId | String |  |
| setUserId | void |  |
| setPkId | void |  |
| setKeyAlg | void |  |
| getKeyAlg | String |  |
| getKeyPem | String |  |
| setKeyPem | void |  |
| getPkId | String |  |
| getCreatedBy | String |  |
| setCreatedBy | void |  |




