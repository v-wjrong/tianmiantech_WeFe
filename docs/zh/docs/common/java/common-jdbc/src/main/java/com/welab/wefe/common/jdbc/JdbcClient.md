# 基础信息

|      |      |
|------|------|
| 名称 | JdbcClient |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-jdbc/src/main/java/com/welab/wefe/common/jdbc/JdbcClient.java |
| 包名 | com.welab.wefe.common.jdbc |
| 依赖项 | ['com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.jdbc.base.DatabaseType', 'com.welab.wefe.common.jdbc.base.JdbcScanner', 'com.welab.wefe.common.jdbc.hive.HiveScanner', 'com.welab.wefe.common.jdbc.mysql.MysqlScanner', 'com.welab.wefe.common.util.StringUtil', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.sql', 'java.util.ArrayList', 'java.util.LinkedHashMap', 'java.util.List', 'java.util.Map', 'java.util.function.Consumer', 'java.util.function.Function'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| JdbcClient | class |  |



## 类 JdbcClient

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | JdbcClient |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| password | String |  |
| host | String |  |
| port | Integer |  |
| LOG = LoggerFactory.getLogger(JdbcClient.class) | Logger |  |
| userName | String |  |
| dbName | String |  |
| databaseType | DatabaseType |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| saveBatch | void |  |
| createScanner | JdbcScanner |  |
| queryList | List<Map<String, Object>> |  |
| createScanner | JdbcScanner |  |
| execute | boolean |  |
| listTables | List<String> |  |
| createConnection | Connection |  |
| selectRowCount | long |  |
| createScanner | JdbcScanner |  |
| scan | void |  |
| testSql | String |  |
| create | JdbcClient |  |
| queryOne | Map<String, Object> |  |
| scan | void |  |
| test | String |  |
| scan | void |  |
| scan | void |  |
| getHeaders | List<String> |  |
| getHeaders | List<String> |  |
| queryOne | Map<String, Object> |  |
| listTableFields | List<String> |  |
| queryList | List<Map<String, Object>> |  |
| saveBatch | void |  |
| createConnection | Connection |  |
| close | void |  |




