# Basic Information

|      |      |
|------|------|
| Name | Account |
| Language | .java |
| Code Path | WeFe/common/java/common-data-mongodb/src/main/java/com/welab/wefe/common/data/mongodb/entity/manager/Account.java |
| Package Name | com.welab.wefe.common.data.mongodb.entity.manager |
| Dependencies | ['com.alibaba.fastjson.JSONArray', 'com.welab.wefe.common.data.mongodb.constant.MongodbTable', 'com.welab.wefe.common.data.mongodb.entity.base.AbstractNormalMongoModel', 'com.welab.wefe.common.wefe.enums.AuditStatus', 'org.springframework.data.mongodb.core.mapping.Document', 'javax.persistence.EnumType', 'javax.persistence.Enumerated', 'java.util.Date', 'java.util.UUID'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| Account | class |  |



## Class Account

|      |      |
|------|------|
| Access Modifier | @Document(collection = MongodbTable.ACCOUNT);public |
| Type | class |
| Name | Account |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
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

### Method List

| Name  | Type  | Description |
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




