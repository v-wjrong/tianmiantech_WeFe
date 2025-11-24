# Basic Information

|      |      |
|------|------|
| Name | AbstractDruidTemplate |
| Language | .java |
| Code Path | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/feature/sql/AbstractDruidTemplate.java |
| Package Name | com.welab.wefe.serving.service.feature.sql |
| Dependencies | ['com.alibaba.druid.pool.DruidDataSource', 'com.alibaba.druid.pool.DruidDataSourceFactory', 'com.alibaba.druid.pool.DruidPooledConnection', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.jdbc.base.DatabaseType', 'java.sql.PreparedStatement', 'java.sql.ResultSet', 'java.sql.SQLException', 'java.util.HashMap', 'java.util.Map'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| AbstractDruidTemplate | class |  |



## Class AbstractDruidTemplate

|      |      |
|------|------|
| Access Modifier | public abstract |
| Type | class |
| Name | AbstractDruidTemplate |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| PROPERTIES = new HashMap<>() | Map<String, Object> |  |
| DRUID_DATA_SOURCE = new HashMap<>() | Map<String, DruidDataSource> |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| url | String |  |
| execute | Map<String, Object> |  |
| driver | String |  |
| getConnection | DruidPooledConnection |  |




