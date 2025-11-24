# 基础信息

|      |      |
|------|------|
| 名称 | TrustCerts |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-data-mongodb/src/main/java/com/welab/wefe/common/data/mongodb/entity/union/TrustCerts.java |
| 包名 | com.welab.wefe.common.data.mongodb.entity.union |
| 依赖项 | ['com.welab.wefe.common.data.mongodb.constant.MongodbTable', 'com.welab.wefe.common.data.mongodb.entity.base.AbstractBlockChainBusinessModel', 'com.welab.wefe.common.data.mongodb.entity.union.ext.TrustCertsExtJSON', 'com.welab.wefe.common.data.mongodb.entity.union.ext.UnionNodeExtJSON', 'org.springframework.data.mongodb.core.mapping.Document'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| TrustCerts | class |  |



## 类 TrustCerts

|      |      |
|------|------|
| 访问范围 | @Document(collection = MongodbTable.Union.TRUST_CERTS);public |
| 类型 | class |
| 名称 | TrustCerts |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
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

### 方法列表

| 名称  | 类型  | 说明 |
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




