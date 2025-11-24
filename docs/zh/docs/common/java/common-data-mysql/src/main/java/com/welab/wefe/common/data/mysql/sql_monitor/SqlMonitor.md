# 基础信息

|      |      |
|------|------|
| 名称 | SqlMonitor |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-data-mysql/src/main/java/com/welab/wefe/common/data/mysql/sql_monitor/SqlMonitor.java |
| 包名 | com.welab.wefe.common.data.mysql.sql_monitor |
| 依赖项 | ['com.alibaba.druid.filter.FilterEventAdapter', 'com.alibaba.druid.proxy.jdbc.JdbcParameter', 'com.alibaba.druid.proxy.jdbc.PreparedStatementProxy', 'com.alibaba.druid.proxy.jdbc.ResultSetProxy', 'com.alibaba.druid.proxy.jdbc.StatementProxy', 'com.alibaba.druid.sql.SQLUtils', 'java.util', 'java.util.concurrent.ConcurrentHashMap'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| SqlMonitor | class |  |



## 类 SqlMonitor

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | SqlMonitor |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| MAX_ERROR_SQL_CATCH_COUNT = 100 | int |  |
| ERROR_SQL_MAP = new LinkedHashMap<>() | LinkedHashMap<Integer, ErrorSql> |  |
| SLOW_SQL_LIMIT = 100 | int |  |
| statementSqlFormatOption = new SQLUtils.FormatOption(false, true) | SQLUtils.FormatOption |  |
| MAX_SLOW_SQL_CATCH_COUNT = 100 | int |  |
| SLOW_SQL_MAP = new ConcurrentHashMap<>() | ConcurrentHashMap<Integer, SlowSql> |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| statementExecuteUpdateAfter | void |  |
| catchErrorSql | void |  |
| statementExecuteBatchAfter | void |  |
| catchSlowSql | void |  |
| getErrorSqlList | Collection<ErrorSql> |  |
| statementExecuteAfter | void |  |
| statementExecuteQueryAfter | void |  |
| getSlowSqlList | List<SlowSql> |  |
| statement_executeErrorAfter | void |  |
| statementExecuteBefore | void |  |
| statementExecuteBatchBefore | void |  |
| statementExecuteQueryBefore | void |  |
| statementExecuteUpdateBefore | void |  |




