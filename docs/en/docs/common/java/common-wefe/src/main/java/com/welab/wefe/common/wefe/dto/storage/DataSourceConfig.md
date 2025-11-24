# Basic Information

|      |      |
|------|------|
| Name | DataSourceConfig |
| Language | .java |
| Code Path | WeFe/common/java/common-wefe/src/main/java/com/welab/wefe/common/wefe/dto/storage/DataSourceConfig.java |
| Package Name | com.welab.wefe.common.wefe.dto.storage |
| Dependencies | ['org.springframework.util.Assert'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| DataSourceConfig | class |  |



## Class DataSourceConfig

|      |      |
|------|------|
| Access Modifier | public abstract |
| Type | class |
| Name | DataSourceConfig |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
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

### Method List

| Name  | Type  | Description |
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




