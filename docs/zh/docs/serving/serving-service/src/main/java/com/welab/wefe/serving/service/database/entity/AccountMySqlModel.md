# 基础信息

|      |      |
|------|------|
| 名称 | AccountMySqlModel |
| 编码语言 | .java |
| 代码路径 | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/database/entity/AccountMySqlModel.java |
| 包名 | com.welab.wefe.serving.service.database.entity |
| 依赖项 | ['com.alibaba.fastjson.JSONArray', 'com.vladmihalcea.hibernate.type.json.JsonStringType', 'com.welab.wefe.common.web.util.DatabaseEncryptConverter', 'com.welab.wefe.common.wefe.enums.AuditStatus', 'org.hibernate.annotations.Type', 'org.hibernate.annotations.TypeDef', 'javax.persistence'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| AccountMySqlModel | class |  |



## 类 AccountMySqlModel

|      |      |
|------|------|
| 访问范围 | @Entity(name = "account");@TypeDef(name = "json", typeClass = JsonStringType.class);public |
| 类型 | class |
| 名称 | AccountMySqlModel |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
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

### 方法列表

| 名称  | 类型  | 说明 |
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




