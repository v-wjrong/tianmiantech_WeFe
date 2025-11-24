# Basic Information

|      |      |
|------|------|
| Name | CertInfo |
| Language | .java |
| Code Path | WeFe/common/java/common-data-mongodb/src/main/java/com/welab/wefe/common/data/mongodb/entity/manager/CertInfo.java |
| Package Name | com.welab.wefe.common.data.mongodb.entity.manager |
| Dependencies | ['java.util.UUID', 'javax.persistence.Column', 'org.springframework.data.mongodb.core.mapping.Document', 'com.welab.wefe.common.data.mongodb.constant.MongodbTable', 'com.welab.wefe.common.data.mongodb.entity.base.AbstractNormalMongoModel'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| CertInfo | class |  |



## Class CertInfo

|      |      |
|------|------|
| Access Modifier | @Document(collection = MongodbTable.CERT_INFO);public |
| Type | class |
| Name | CertInfo |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| pCertId | String |  |
| createdBy | String |  |
| subjectOrg | String |  |
| subjectKeyId | String |  |
| pkId = UUID.randomUUID().toString().replaceAll("-", "") | String |  |
| issuerKeyId | String |  |
| userId | String |  |
| updateStatusReason | String |  |
| issuerOrg | String |  |
| subjectPubKey | String |  |
| isCACert | Boolean |  |
| csrId | String |  |
| isRootCert | Boolean |  |
| subjectCN | String |  |
| certContent | String |  |
| issuerCN | String |  |
| serialNumber | String |  |
| serialVersionUID = 2536000530329139954L | long |  |
| status | int |  |
| canTrust | Boolean |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getIssuerOrg | String |  |
| setCertContent | void |  |
| setPkId | void |  |
| setIsRootCert | void |  |
| setIssuerCN | void |  |
| setSubjectPubKey | void |  |
| getIssuerKeyId | String |  |
| getSerialNumber | String |  |
| setIssuerOrg | void |  |
| getCsrId | String |  |
| getPkId | String |  |
| getpCertId | String |  |
| setSubjectCN | void |  |
| setpCertId | void |  |
| setStatus | void |  |
| getIsCACert | Boolean |  |
| getCertContent | String |  |
| getUserId | String |  |
| getSubjectOrg | String |  |
| getCanTrust | Boolean |  |
| setCanTrust | void |  |
| getUpdateStatusReason | String |  |
| setUpdateStatusReason | void |  |
| setSerialNumber | void |  |
| getSubjectKeyId | String |  |
| setIssuerKeyId | void |  |
| setCreatedBy | void |  |
| getCreatedBy | String |  |
| setCsrId | void |  |
| setUserId | void |  |
| setSubjectOrg | void |  |
| setSubjectKeyId | void |  |
| setIsCACert | void |  |
| getIsRootCert | Boolean |  |
| getStatus | int |  |
| getIssuerCN | String |  |
| getSubjectCN | String |  |
| getSubjectPubKey | String |  |




