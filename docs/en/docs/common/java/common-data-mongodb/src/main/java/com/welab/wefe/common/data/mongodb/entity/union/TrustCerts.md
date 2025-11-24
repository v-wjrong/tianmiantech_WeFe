# Basic Information

|      |      |
|------|------|
| Name | TrustCerts |
| Language | .java |
| Code Path | WeFe/common/java/common-data-mongodb/src/main/java/com/welab/wefe/common/data/mongodb/entity/union/TrustCerts.java |
| Package Name | com.welab.wefe.common.data.mongodb.entity.union |
| Dependencies | ['com.welab.wefe.common.data.mongodb.constant.MongodbTable', 'com.welab.wefe.common.data.mongodb.entity.base.AbstractBlockChainBusinessModel', 'com.welab.wefe.common.data.mongodb.entity.union.ext.TrustCertsExtJSON', 'com.welab.wefe.common.data.mongodb.entity.union.ext.UnionNodeExtJSON', 'org.springframework.data.mongodb.core.mapping.Document'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| TrustCerts | class |  |



## Class TrustCerts

|      |      |
|------|------|
| Access Modifier | @Document(collection = MongodbTable.Union.TRUST_CERTS);public |
| Type | class |
| Name | TrustCerts |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| certId | String |  |
| issuerCn | String |  |
| serialNumber | String |  |
| extJson = new TrustCertsExtJSON() | TrustCertsExtJSON |  |
| subjectCn | String |  |
| issuerOrg | String |  |
| pCertId | String |  |
| certContent | String |  |
| isCaCert | String |  |
| isRootCert | String |  |
| subjectOrg | String |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getIssuerCn | String |  |
| getSerialNumber | String |  |
| setCertId | void |  |
| setIssuerCn | void |  |
| setIssuerOrg | void |  |
| getpCertId | String |  |
| setSubjectCn | void |  |
| setSubjectOrg | void |  |
| getCertContent | String |  |
| getCertId | String |  |
| setSerialNumber | void |  |
| setpCertId | void |  |
| getSubjectOrg | String |  |
| getIssuerOrg | String |  |
| getSubjectCn | String |  |
| setCertContent | void |  |
| getIsCaCert | String |  |
| setIsCaCert | void |  |
| getIsRootCert | String |  |
| setIsRootCert | void |  |
| getExtJson | TrustCertsExtJSON |  |
| setExtJson | void |  |




