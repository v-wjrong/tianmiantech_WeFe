# Basic Information

|      |      |
|------|------|
| Name | RedisIntermediateCache |
| Language | .java |
| Code Path | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/utils/RedisIntermediateCache.java |
| Package Name | com.welab.wefe.serving.service.utils |
| Dependencies | ['org.apache.commons.lang3.StringUtils', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'com.welab.wefe.mpc.cache.intermediate.CacheOperation', 'redis.clients.jedis.Jedis', 'redis.clients.jedis.JedisPool', 'redis.clients.jedis.JedisPoolConfig'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| RedisIntermediateCache | class |  |



## Class RedisIntermediateCache

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | RedisIntermediateCache |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| password | String |  |
| LOG = LoggerFactory.getLogger(RedisIntermediateCache.class) | Logger |  |
| jedisPool = null | JedisPool |  |
| port | int |  |
| host | String |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| get | Object |  |
| getJedisPoolInstance | JedisPool |  |
| save | void |  |
| delete | void |  |




