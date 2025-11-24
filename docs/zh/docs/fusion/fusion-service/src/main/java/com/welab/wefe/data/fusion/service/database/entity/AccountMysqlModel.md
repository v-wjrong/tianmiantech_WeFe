# 基础信息

|      |      |
|------|------|
| 名称 | AccountMysqlModel |
| 编码语言 | .java |
| 代码路径 | WeFe/fusion/fusion-service/src/main/java/com/welab/wefe/data/fusion/service/database/entity/AccountMysqlModel.java |
| 包名 | com.welab.wefe.data.fusion.service.database.entity |
| 依赖项 | ['com.alibaba.fastjson.JSONArray', 'com.vladmihalcea.hibernate.type.json.JsonStringType', 'com.welab.wefe.common.web.util.DatabaseEncryptConverter', 'com.welab.wefe.common.wefe.enums.AuditStatus', 'org.hibernate.annotations.Type', 'org.hibernate.annotations.TypeDef', 'javax.persistence', 'java.util.Date'] |
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

### 方法列表

| 名称  | 类型  | 说明 |
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




