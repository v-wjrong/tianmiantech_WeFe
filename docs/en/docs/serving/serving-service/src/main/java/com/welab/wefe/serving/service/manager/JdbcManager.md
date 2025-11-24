# Basic Information

|      |      |
|------|------|
| Name | JdbcManager |
| Language | .java |
| Code Path | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/manager/JdbcManager.java |
| Package Name | com.welab.wefe.serving.service.manager |
| Dependencies | ['java.sql.Connection', 'java.sql.DriverManager', 'java.sql.PreparedStatement', 'java.sql.ResultSet', 'java.sql.SQLException', 'java.util.ArrayList', 'java.util.HashMap', 'java.util.LinkedHashMap', 'java.util.List', 'java.util.Map', 'java.util.Set', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'com.nimbusds.jose.shaded.json.JSONObject', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.jdbc.base.DatabaseType'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| JdbcManager | class |  |



## Class JdbcManager

|      |      |
|------|------|
| Access Modifier | @Deprecated;public |
| Type | class |
| Name | JdbcManager |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| log = LoggerFactory.getLogger(JdbcManager.class) | Logger |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| batchInsert | void |  |
| queryOne | Map<String, String> |  |
| queryListByIds | List<Map<String, String>> |  |
| getConnection | Connection |  |
| queryList | List<Map<String, String>> |  |
| testQuery | boolean |  |
| queryListByConditions | List<Map<String, String>> |  |
| update | boolean |  |
| batchQuerySql | Map<String, String> |  |
| getConnection | Connection |  |
| execute | boolean |  |
| close | void |  |
| queryTableFields | Map<String, String> |  |
| queryTables | List<String> |  |
| count | long |  |
| close | void |  |




