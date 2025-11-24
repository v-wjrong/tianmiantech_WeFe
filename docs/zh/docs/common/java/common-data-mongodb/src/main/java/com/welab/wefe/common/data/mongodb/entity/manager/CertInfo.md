# 基础信息

|      |      |
|------|------|
| 名称 | CertInfo |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-data-mongodb/src/main/java/com/welab/wefe/common/data/mongodb/entity/manager/CertInfo.java |
| 包名 | com.welab.wefe.common.data.mongodb.entity.manager |
| 依赖项 | ['java.util.UUID', 'javax.persistence.Column', 'org.springframework.data.mongodb.core.mapping.Document', 'com.welab.wefe.common.data.mongodb.constant.MongodbTable', 'com.welab.wefe.common.data.mongodb.entity.base.AbstractNormalMongoModel'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| CertInfo | class |  |



## 类 CertInfo

|      |      |
|------|------|
| 访问范围 | @Document(collection = MongodbTable.CERT_INFO);public |
| 类型 | class |
| 名称 | CertInfo |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
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

### 方法列表

| 名称  | 类型  | 说明 |
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




