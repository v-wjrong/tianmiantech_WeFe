# 基础信息

|      |      |
|------|------|
| 名称 | JdbcManager |
| 编码语言 | .java |
| 代码路径 | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/manager/JdbcManager.java |
| 包名 | com.welab.wefe.serving.service.manager |
| 依赖项 | ['java.sql.Connection', 'java.sql.DriverManager', 'java.sql.PreparedStatement', 'java.sql.ResultSet', 'java.sql.SQLException', 'java.util.ArrayList', 'java.util.HashMap', 'java.util.LinkedHashMap', 'java.util.List', 'java.util.Map', 'java.util.Set', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'com.nimbusds.jose.shaded.json.JSONObject', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.jdbc.base.DatabaseType'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| JdbcManager | class |  |



## 类 JdbcManager

|      |      |
|------|------|
| 访问范围 | @Deprecated;public |
| 类型 | class |
| 名称 | JdbcManager |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| log = LoggerFactory.getLogger(JdbcManager.class) | Logger |  |

### 方法列表

| 名称  | 类型  | 说明 |
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




