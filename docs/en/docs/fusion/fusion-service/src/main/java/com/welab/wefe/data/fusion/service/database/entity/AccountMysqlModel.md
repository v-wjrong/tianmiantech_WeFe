# Basic Information

|      |      |
|------|------|
| Name | AccountMysqlModel |
| Language | .java |
| Code Path | WeFe/fusion/fusion-service/src/main/java/com/welab/wefe/data/fusion/service/database/entity/AccountMysqlModel.java |
| Package Name | com.welab.wefe.data.fusion.service.database.entity |
| Dependencies | ['com.alibaba.fastjson.JSONArray', 'com.vladmihalcea.hibernate.type.json.JsonStringType', 'com.welab.wefe.common.web.util.DatabaseEncryptConverter', 'com.welab.wefe.common.wefe.enums.AuditStatus', 'org.hibernate.annotations.Type', 'org.hibernate.annotations.TypeDef', 'javax.persistence', 'java.util.Date'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| AccountMysqlModel | class |  |



## Class AccountMysqlModel

|      |      |
|------|------|
| Access Modifier | @Entity(name = "account");@TypeDef(name = "json", typeClass = JsonStringType.class);public |
| Type | class |
| Name | AccountMysqlModel |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| password | String |  |
| auditComment | String |  |
| cancelled | boolean |  |
| enable | Boolean |  |
| auditStatus | AuditStatus |  |
| historyPasswordList | JSONArray |  |
| nickname | String |  |
| salt | String |  |
| superAdminRole | Boolean |  |
| adminRole | Boolean |  |
| email | String |  |
| phoneNumber | String |  |
| lastActionTime | Date |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| setNickname | void |  |
| isCancelled | boolean |  |
| setPassword | void |  |
| getSalt | String |  |
| setCancelled | void |  |
| setEmail | void |  |
| getAuditStatus | AuditStatus |  |
| setAdminRole | void |  |
| setSuperAdminRole | void |  |
| getHistoryPasswordList | JSONArray |  |
| setHistoryPasswordList | void |  |
| getLastActionTime | Date |  |
| setLastActionTime | void |  |
| getSuperAdminRole | Boolean |  |
| getAdminRole | Boolean |  |
| getPassword | String |  |
| getNickname | String |  |
| setPhoneNumber | void |  |
| getEnable | Boolean |  |
| setAuditComment | void |  |
| getEmail | String |  |
| setEnable | void |  |
| setSalt | void |  |
| setAuditStatus | void |  |
| getPhoneNumber | String |  |
| getAuditComment | String |  |




