# 基础信息

|      |      |
|------|------|
| 名称 | DataSourceMysqlModel |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/database/entity/DataSourceMysqlModel.java |
| 包名 | com.welab.wefe.board.service.database.entity |
| 依赖项 | ['com.welab.wefe.board.service.database.entity.base.AbstractBaseMySqlModel', 'com.welab.wefe.common.jdbc.base.DatabaseType', 'com.welab.wefe.common.web.util.DatabaseEncryptConverter', 'javax.persistence.Convert', 'javax.persistence.Entity', 'javax.persistence.EnumType', 'javax.persistence.Enumerated'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| DataSourceMysqlModel | class |  |



## 类 DataSourceMysqlModel

|      |      |
|------|------|
| 访问范围 | @Entity(name = "data_source");public |
| 类型 | class |
| 名称 | DataSourceMysqlModel |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| name | String |  |
| port | Integer |  |
| userName | String |  |
| password | String |  |
| databaseName | String |  |
| databaseType | DatabaseType |  |
| host | String |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| setDatabaseType | void |  |
| setUserName | void |  |
| getDatabaseName | String |  |
| setPort | void |  |
| getDatabaseType | DatabaseType |  |
| getHost | String |  |
| setHost | void |  |
| setName | void |  |
| setPassword | void |  |
| getName | String |  |
| getUserName | String |  |
| getPassword | String |  |
| setDatabaseName | void |  |
| getPort | Integer |  |




