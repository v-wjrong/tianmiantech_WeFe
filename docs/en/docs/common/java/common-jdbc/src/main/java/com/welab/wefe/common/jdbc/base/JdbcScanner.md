# Basic Information

|      |      |
|------|------|
| Name | JdbcScanner |
| Language | .java |
| Code Path | WeFe/common/java/common-jdbc/src/main/java/com/welab/wefe/common/jdbc/base/JdbcScanner.java |
| Package Name | com.welab.wefe.common.jdbc.base |
| Dependencies | ['com.welab.wefe.common.jdbc.JdbcClient', 'org.apache.commons.collections4.CollectionUtils', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.io.Closeable', 'java.io.IOException', 'java.sql', 'java.util.LinkedHashMap', 'java.util.List'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| JdbcScanner | class |  |



## Class JdbcScanner

|      |      |
|------|------|
| Access Modifier | public abstract |
| Type | class |
| Name | JdbcScanner |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| headers | List<String> |  |
| sql | String |  |
| resultSet = null | ResultSet |  |
| statement = null | PreparedStatement |  |
| conn | Connection |  |
| maxReadLine | long |  |
| LOG = LoggerFactory.getLogger(this.getClass()) | Logger |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| readOneRow | LinkedHashMap<String, Object> |  |
| execute | ResultSet |  |
| close | void |  |




