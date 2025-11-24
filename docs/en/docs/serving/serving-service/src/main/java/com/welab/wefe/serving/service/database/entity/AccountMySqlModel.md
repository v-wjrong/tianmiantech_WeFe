# Basic Information

|      |      |
|------|------|
| Name | AccountMySqlModel |
| Language | .java |
| Code Path | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/database/entity/AccountMySqlModel.java |
| Package Name | com.welab.wefe.serving.service.database.entity |
| Dependencies | ['com.alibaba.fastjson.JSONArray', 'com.vladmihalcea.hibernate.type.json.JsonStringType', 'com.welab.wefe.common.web.util.DatabaseEncryptConverter', 'com.welab.wefe.common.wefe.enums.AuditStatus', 'org.hibernate.annotations.Type', 'org.hibernate.annotations.TypeDef', 'javax.persistence'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| AccountMySqlModel | class |  |



## Class AccountMySqlModel

|      |      |
|------|------|
| Access Modifier | @Entity(name = "account");@TypeDef(name = "json", typeClass = JsonStringType.class);public |
| Type | class |
| Name | AccountMySqlModel |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| password | String |  |
| auditStatus | AuditStatus |  |
| nickname | String |  |
| serialVersionUID = -6835962000573567824L | long |  |
| enable | Boolean |  |
| superAdminRole | Boolean |  |
| historyPasswordList | JSONArray |  |
| auditComment | String |  |
| cancelled = false | boolean |  |
| email | String |  |
| salt | String |  |
| adminRole | Boolean |  |
| phoneNumber | String |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| setAuditComment | void |  |
| setCancelled | void |  |
| setAdminRole | void |  |
| getNickname | String |  |
| getEnable | Boolean |  |
| isCancelled | boolean |  |
| getAuditComment | String |  |
| getSalt | String |  |
| setSuperAdminRole | void |  |
| getPhoneNumber | String |  |
| getSuperAdminRole | Boolean |  |
| getEmail | String |  |
| getAdminRole | Boolean |  |
| setNickname | void |  |
| setPhoneNumber | void |  |
| setPassword | void |  |
| setEnable | void |  |
| setAuditStatus | void |  |
| getAuditStatus | AuditStatus |  |
| setEmail | void |  |
| setSalt | void |  |
| getPassword | String |  |
| getHistoryPasswordList | JSONArray |  |
| setHistoryPasswordList | void |  |




