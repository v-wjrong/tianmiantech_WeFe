# 基础信息

|      |      |
|------|------|
| 名称 | AccountMysqlModel |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/database/entity/AccountMysqlModel.java |
| 包名 | com.welab.wefe.board.service.database.entity |
| 依赖项 | ['com.alibaba.fastjson.JSONArray', 'com.alibaba.fastjson.JSONObject', 'com.vladmihalcea.hibernate.type.json.JsonStringType', 'com.welab.wefe.board.service.database.entity.base.AbstractBaseMySqlModel', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.web.util.DatabaseEncryptConverter', 'com.welab.wefe.common.wefe.enums.AuditStatus', 'org.hibernate.annotations.Type', 'org.hibernate.annotations.TypeDef', 'javax.persistence', 'java.util.Date'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| AccountMysqlModel | class |  |



## 类 AccountMysqlModel

|      |      |
|------|------|
| 访问范围 | @Entity(name = "account");@TypeDef(name = "json", typeClass = JsonStringType.class);public |
| 类型 | class |
| 名称 | AccountMysqlModel |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
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

### 方法列表

| 名称  | 类型  | 说明 |
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




