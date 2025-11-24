# 基础信息

|      |      |
|------|------|
| 名称 | AbstractDruidTemplate |
| 编码语言 | .java |
| 代码路径 | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/feature/sql/AbstractDruidTemplate.java |
| 包名 | com.welab.wefe.serving.service.feature.sql |
| 依赖项 | ['com.alibaba.druid.pool.DruidDataSource', 'com.alibaba.druid.pool.DruidDataSourceFactory', 'com.alibaba.druid.pool.DruidPooledConnection', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.jdbc.base.DatabaseType', 'java.sql.PreparedStatement', 'java.sql.ResultSet', 'java.sql.SQLException', 'java.util.HashMap', 'java.util.Map'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| AbstractDruidTemplate | class |  |



## 类 AbstractDruidTemplate

|      |      |
|------|------|
| 访问范围 | public abstract |
| 类型 | class |
| 名称 | AbstractDruidTemplate |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| PROPERTIES = new HashMap<>() | Map<String, Object> |  |
| DRUID_DATA_SOURCE = new HashMap<>() | Map<String, DruidDataSource> |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| url | String |  |
| execute | Map<String, Object> |  |
| driver | String |  |
| getConnection | DruidPooledConnection |  |




