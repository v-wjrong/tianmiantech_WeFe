# 基础信息

|      |      |
|------|------|
| 名称 | JdbcScanner |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-jdbc/src/main/java/com/welab/wefe/common/jdbc/base/JdbcScanner.java |
| 包名 | com.welab.wefe.common.jdbc.base |
| 依赖项 | ['com.welab.wefe.common.jdbc.JdbcClient', 'org.apache.commons.collections4.CollectionUtils', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.io.Closeable', 'java.io.IOException', 'java.sql', 'java.util.LinkedHashMap', 'java.util.List'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| JdbcScanner | class |  |



## 类 JdbcScanner

|      |      |
|------|------|
| 访问范围 | public abstract |
| 类型 | class |
| 名称 | JdbcScanner |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| headers | List<String> |  |
| sql | String |  |
| resultSet = null | ResultSet |  |
| statement = null | PreparedStatement |  |
| conn | Connection |  |
| maxReadLine | long |  |
| LOG = LoggerFactory.getLogger(this.getClass()) | Logger |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| readOneRow | LinkedHashMap<String, Object> |  |
| execute | ResultSet |  |
| close | void |  |




