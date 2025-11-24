# Basic Information

|      |      |
|------|------|
| Name | SqlMonitor |
| Language | .java |
| Code Path | WeFe/common/java/common-data-mysql/src/main/java/com/welab/wefe/common/data/mysql/sql_monitor/SqlMonitor.java |
| Package Name | com.welab.wefe.common.data.mysql.sql_monitor |
| Dependencies | ['com.alibaba.druid.filter.FilterEventAdapter', 'com.alibaba.druid.proxy.jdbc.JdbcParameter', 'com.alibaba.druid.proxy.jdbc.PreparedStatementProxy', 'com.alibaba.druid.proxy.jdbc.ResultSetProxy', 'com.alibaba.druid.proxy.jdbc.StatementProxy', 'com.alibaba.druid.sql.SQLUtils', 'java.util', 'java.util.concurrent.ConcurrentHashMap'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| SqlMonitor | class |  |



## Class SqlMonitor

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | SqlMonitor |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| MAX_ERROR_SQL_CATCH_COUNT = 100 | int |  |
| ERROR_SQL_MAP = new LinkedHashMap<>() | LinkedHashMap<Integer, ErrorSql> |  |
| SLOW_SQL_LIMIT = 100 | int |  |
| statementSqlFormatOption = new SQLUtils.FormatOption(false, true) | SQLUtils.FormatOption |  |
| MAX_SLOW_SQL_CATCH_COUNT = 100 | int |  |
| SLOW_SQL_MAP = new ConcurrentHashMap<>() | ConcurrentHashMap<Integer, SlowSql> |  |

### Method List

| Name  | Type  | Description |
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




