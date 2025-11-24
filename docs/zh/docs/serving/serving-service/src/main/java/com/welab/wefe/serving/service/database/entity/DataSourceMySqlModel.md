# 基础信息

|      |      |
|------|------|
| 名称 | DataSourceMySqlModel |
| 编码语言 | .java |
| 代码路径 | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/database/entity/DataSourceMySqlModel.java |
| 包名 | com.welab.wefe.serving.service.database.entity |
| 依赖项 | ['com.welab.wefe.common.jdbc.base.DatabaseType', 'com.welab.wefe.common.web.util.DatabaseEncryptConverter', 'javax.persistence'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| DataSourceMySqlModel | class |  |



## 类 DataSourceMySqlModel

|      |      |
|------|------|
| 访问范围 | @Entity(name = "data_source");public |
| 类型 | class |
| 名称 | DataSourceMySqlModel |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| serialVersionUID = 4348703828245457696L | long |  |
| port | Integer |  |
| password | String |  |
| databaseName | String |  |
| host | String |  |
| PASSWORD_MASK = "*************" | String |  |
| userName | String |  |
| databaseType | DatabaseType |  |
| name | String |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| setDatabaseName | void |  |
| setHost | void |  |
| getDatabaseName | String |  |
| setDatabaseType | void |  |
| getName | String |  |
| getPort | Integer |  |
| getUserName | String |  |
| getHost | String |  |
| setPort | void |  |
| setName | void |  |
| getDatabaseType | DatabaseType |  |
| setUserName | void |  |
| getPassword | String |  |
| setPassword | void |  |




