# Basic Information

|      |      |
|------|------|
| Name | JdbcClient |
| Language | .java |
| Code Path | WeFe/common/java/common-jdbc/src/main/java/com/welab/wefe/common/jdbc/JdbcClient.java |
| Package Name | com.welab.wefe.common.jdbc |
| Dependencies | ['com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.jdbc.base.DatabaseType', 'com.welab.wefe.common.jdbc.base.JdbcScanner', 'com.welab.wefe.common.jdbc.hive.HiveScanner', 'com.welab.wefe.common.jdbc.mysql.MysqlScanner', 'com.welab.wefe.common.util.StringUtil', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.sql', 'java.util.ArrayList', 'java.util.LinkedHashMap', 'java.util.List', 'java.util.Map', 'java.util.function.Consumer', 'java.util.function.Function'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| JdbcClient | class |  |



## Class JdbcClient

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | JdbcClient |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| password | String |  |
| host | String |  |
| port | Integer |  |
| LOG = LoggerFactory.getLogger(JdbcClient.class) | Logger |  |
| userName | String |  |
| dbName | String |  |
| databaseType | DatabaseType |  |

### Method List

| Name  | Type  | Description |
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




