# Basic Information

|      |      |
|------|------|
| Name | CertRequestInfo |
| Language | .java |
| Code Path | WeFe/common/java/common-data-mongodb/src/main/java/com/welab/wefe/common/data/mongodb/entity/manager/CertRequestInfo.java |
| Package Name | com.welab.wefe.common.data.mongodb.entity.manager |
| Dependencies | ['java.util.UUID', 'org.springframework.data.mongodb.core.mapping.Document', 'com.welab.wefe.common.data.mongodb.constant.MongodbTable', 'com.welab.wefe.common.data.mongodb.entity.base.AbstractNormalMongoModel'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| CertRequestInfo | class |  |



## Class CertRequestInfo

|      |      |
|------|------|
| Access Modifier | @Document(collection = MongodbTable.CERT_REQUEST_INFO);public |
| Type | class |
| Name | CertRequestInfo |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| issue | Boolean |  |
| createdBy | String |  |
| subjectCN | String |  |
| certRequestContent | String |  |
| issuerCertId | String |  |
| serialVersionUID = 7150886210876056683L | long |  |
| issuerCertUserId | String |  |
| subjectKeyId | String |  |
| userId | String |  |
| pkId = UUID.randomUUID().toString().replaceAll("-", "") | String |  |
| subjectOrg | String |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getSubjectCN | String |  |
| setPkId | void |  |
| getUserId | String |  |
| setIssuerCertUserId | void |  |
| setUserId | void |  |
| setIssuerCertId | void |  |
| setSubjectKeyId | void |  |
| setSubjectCN | void |  |
| getSubjectOrg | String |  |
| setCertRequestContent | void |  |
| getSubjectKeyId | String |  |
| getIssue | Boolean |  |
| setSubjectOrg | void |  |
| getIssuerCertUserId | String |  |
| getCertRequestContent | String |  |
| getPkId | String |  |
| getIssuerCertId | String |  |
| setIssue | void |  |
| getCreatedBy | String |  |
| setCreatedBy | void |  |




