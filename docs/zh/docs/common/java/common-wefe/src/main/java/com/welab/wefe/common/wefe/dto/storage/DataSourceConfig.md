# 基础信息

|      |      |
|------|------|
| 名称 | DataSourceConfig |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-wefe/src/main/java/com/welab/wefe/common/wefe/dto/storage/DataSourceConfig.java |
| 包名 | com.welab.wefe.common.wefe.dto.storage |
| 依赖项 | ['org.springframework.util.Assert'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| DataSourceConfig | class |  |



## 类 DataSourceConfig

|      |      |
|------|------|
| 访问范围 | public abstract |
| 类型 | class |
| 名称 | DataSourceConfig |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| removeAbandonedTimeout = 60 | Integer |  |
| minIdle = 1 | Integer |  |
| removeAbandoned = true | boolean |  |
| testWhileIdle = false | boolean |  |
| url = "jdbc:clickhouse//127.0.0.1:8123" | String |  |
| minEvictableIdleTimeMillis = 60000 | Integer |  |
| validationQuery = "SELECT 1" | String |  |
| maxActive = 50 | Integer |  |
| logAbandoned = true | boolean |  |
| driverClassName | String |  |
| optimalInsertByteSize = 1 | double |  |
| port = 8123 | Integer |  |
| timeBetweenEvictionRunsMillis = 15000 | Integer |  |
| initialSize = 1 | Integer |  |
| password | String |  |
| maxWait = 60000 | Integer |  |
| username | String |  |
| host = "127.0.0.1" | String |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getUrl | String |  |
| setLogAbandoned | void |  |
| buildUrl | void |  |
| setRemoveAbandonedTimeout | void |  |
| getValidationQuery | String |  |
| getUsername | String |  |
| setTimeBetweenEvictionRunsMillis | void |  |
| setUsername | void |  |
| getDriverClassName | String |  |
| getRemoveAbandonedTimeout | Integer |  |
| getMaxWait | Integer |  |
| getMinEvictableIdleTimeMillis | Integer |  |
| isRemoveAbandoned | boolean |  |
| setTestWhileIdle | void |  |
| getInitialSize | Integer |  |
| setUrl | void |  |
| setOptimalInsertByteSize | void |  |
| setValidationQuery | void |  |
| setHost | void |  |
| getMaxActive | Integer |  |
| setInitialSize | void |  |
| setMinIdle | void |  |
| getHost | String |  |
| setRemoveAbandoned | void |  |
| getPort | Integer |  |
| getTimeBetweenEvictionRunsMillis | Integer |  |
| isTestWhileIdle | boolean |  |
| setMaxActive | void |  |
| setMinEvictableIdleTimeMillis | void |  |
| getMinIdle | Integer |  |
| getOptimalInsertByteSize | double |  |
| isLogAbandoned | boolean |  |
| setPort | void |  |
| getPassword | String |  |
| setMaxWait | void |  |
| setPassword | void |  |




