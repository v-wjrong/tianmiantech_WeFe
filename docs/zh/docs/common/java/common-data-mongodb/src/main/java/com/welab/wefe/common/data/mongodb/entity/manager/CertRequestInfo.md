# 基础信息

|      |      |
|------|------|
| 名称 | CertRequestInfo |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-data-mongodb/src/main/java/com/welab/wefe/common/data/mongodb/entity/manager/CertRequestInfo.java |
| 包名 | com.welab.wefe.common.data.mongodb.entity.manager |
| 依赖项 | ['java.util.UUID', 'org.springframework.data.mongodb.core.mapping.Document', 'com.welab.wefe.common.data.mongodb.constant.MongodbTable', 'com.welab.wefe.common.data.mongodb.entity.base.AbstractNormalMongoModel'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| CertRequestInfo | class |  |



## 类 CertRequestInfo

|      |      |
|------|------|
| 访问范围 | @Document(collection = MongodbTable.CERT_REQUEST_INFO);public |
| 类型 | class |
| 名称 | CertRequestInfo |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
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

### 方法列表

| 名称  | 类型  | 说明 |
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




