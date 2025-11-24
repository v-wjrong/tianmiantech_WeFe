# 基础信息

|      |      |
|------|------|
| 名称 | CertKeyInfo |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-data-mongodb/src/main/java/com/welab/wefe/common/data/mongodb/entity/manager/CertKeyInfo.java |
| 包名 | com.welab.wefe.common.data.mongodb.entity.manager |
| 依赖项 | ['java.util.UUID', 'org.springframework.data.mongodb.core.mapping.Document', 'com.welab.wefe.common.data.mongodb.constant.MongodbTable', 'com.welab.wefe.common.data.mongodb.entity.base.AbstractNormalMongoModel', 'com.welab.wefe.common.exception.StatusCodeWithException'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| CertKeyInfo | class |  |



## 类 CertKeyInfo

|      |      |
|------|------|
| 访问范围 | @Document(collection = MongodbTable.CERT_KEY_INFO);public |
| 类型 | class |
| 名称 | CertKeyInfo |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| userId | String |  |
| keyAlg | String |  |
| pkId = UUID.randomUUID().toString().replaceAll("-", "") | String |  |
| serialVersionUID = -7731011364389900165L | long |  |
| createdBy | String |  |
| keyPem | String |  |

### 方法列表

| 名称  | 类型  | 说明 |
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




