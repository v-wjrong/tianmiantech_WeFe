# 基础信息

|      |      |
|------|------|
| 名称 | Account |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-data-mongodb/src/main/java/com/welab/wefe/common/data/mongodb/entity/manager/Account.java |
| 包名 | com.welab.wefe.common.data.mongodb.entity.manager |
| 依赖项 | ['com.alibaba.fastjson.JSONArray', 'com.welab.wefe.common.data.mongodb.constant.MongodbTable', 'com.welab.wefe.common.data.mongodb.entity.base.AbstractNormalMongoModel', 'com.welab.wefe.common.wefe.enums.AuditStatus', 'org.springframework.data.mongodb.core.mapping.Document', 'javax.persistence.EnumType', 'javax.persistence.Enumerated', 'java.util.Date', 'java.util.UUID'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| Account | class |  |



## 类 Account

|      |      |
|------|------|
| 访问范围 | @Document(collection = MongodbTable.ACCOUNT);public |
| 类型 | class |
| 名称 | Account |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| adminRole | Boolean |  |
| superAdminRole | Boolean |  |
| phoneNumber | String |  |
| needUpdatePassword | boolean |  |
| accountId = UUID.randomUUID().toString().replaceAll("-", "") | String |  |
| salt | String |  |
| historyPasswordList | JSONArray |  |
| nickname | String |  |
| lastActionTime | Date |  |
| cancelled | boolean |  |
| password | String |  |
| enable | Boolean |  |
| auditComment | String |  |
| auditStatus | AuditStatus |  |
| updatedBy | String |  |
| email | String |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getAuditComment | String |  |
| getSalt | String |  |
| setEnable | void |  |
| setNickname | void |  |
| getAccountId | String |  |
| setPhoneNumber | void |  |
| getEmail | String |  |
| getPhoneNumber | String |  |
| getEnable | Boolean |  |
| getPassword | String |  |
| setAccountId | void |  |
| setSuperAdminRole | void |  |
| getAdminRole | Boolean |  |
| setCancelled | void |  |
| getHistoryPasswordList | JSONArray |  |
| setHistoryPasswordList | void |  |
| getUpdatedBy | String |  |
| setUpdatedBy | void |  |
| isCancelled | boolean |  |
| setSalt | void |  |
| isNeedUpdatePassword | boolean |  |
| getNickname | String |  |
| setEmail | void |  |
| setNeedUpdatePassword | void |  |
| setAuditStatus | void |  |
| setAdminRole | void |  |
| getSuperAdminRole | Boolean |  |
| setLastActionTime | void |  |
| getLastActionTime | Date |  |
| setAuditComment | void |  |
| setPassword | void |  |
| getAuditStatus | AuditStatus |  |




