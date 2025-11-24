# Basic Information

|      |      |
|------|------|
| Name | AccountMysqlModel |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/database/entity/AccountMysqlModel.java |
| Package Name | com.welab.wefe.board.service.database.entity |
| Dependencies | ['com.alibaba.fastjson.JSONArray', 'com.alibaba.fastjson.JSONObject', 'com.vladmihalcea.hibernate.type.json.JsonStringType', 'com.welab.wefe.board.service.database.entity.base.AbstractBaseMySqlModel', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.web.util.DatabaseEncryptConverter', 'com.welab.wefe.common.wefe.enums.AuditStatus', 'org.hibernate.annotations.Type', 'org.hibernate.annotations.TypeDef', 'javax.persistence', 'java.util.Date'] |
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
| cancelled | boolean |  |
| email | String |  |
| password | String |  |
| enable | Boolean |  |
| auditComment | String |  |
| historyPasswordList | JSONArray |  |
| nickname | String |  |
| phoneNumber | String |  |
| uiConfig | JSONObject |  |
| auditStatus | AuditStatus |  |
| adminRole | Boolean |  |
| lastActionTime | Date |  |
| salt | String |  |
| superAdminRole | Boolean |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| setNickname | void |  |
| setEmail | void |  |
| getEnable | Boolean |  |
| setAuditStatus | void |  |
| getSuperAdminRole | Boolean |  |
| getAuditComment | String |  |
| setEnable | void |  |
| getAdminRole | Boolean |  |
| getEmail | String |  |
| getSalt | String |  |
| setPassword | void |  |
| setPhoneNumber | void |  |
| setSuperAdminRole | void |  |
| setAdminRole | void |  |
| setCancelled | void |  |
| getLastActionTime | Date |  |
| setLastActionTime | void |  |
| getHistoryPasswordList | JSONArray |  |
| setHistoryPasswordList | void |  |
| getUiConfig | JSONObject |  |
| getNickname | String |  |
| getPhoneNumber | String |  |
| isCancelled | boolean |  |
| getAuditStatus | AuditStatus |  |
| setSalt | void |  |
| getPassword | String |  |
| setAuditComment | void |  |
| setUiConfig | void |  |




