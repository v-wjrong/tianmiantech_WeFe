# 基础信息

|      |      |
|------|------|
| 名称 | SlowSql |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-data-mysql/src/main/java/com/welab/wefe/common/data/mysql/sql_monitor/SlowSql.java |
| 包名 | com.welab.wefe.common.data.mysql.sql_monitor |
| 依赖项 | ['java.util.Date'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| SlowSql | class |  |



## 类 SlowSql

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | SlowSql |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| avgSpend | long |  |
| sql | String |  |
| minSpend | long |  |
| sqlHash | int |  |
| firstCatchTime = new Date() | Date |  |
| maxSpend | long |  |
| catchCount | int |  |
| FASTEST_SQL | SlowSql |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| catchOnce | void |  |




