# 基础信息

|      |      |
|------|------|
| 名称 | RedisIntermediateCache |
| 编码语言 | .java |
| 代码路径 | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/utils/RedisIntermediateCache.java |
| 包名 | com.welab.wefe.serving.service.utils |
| 依赖项 | ['org.apache.commons.lang3.StringUtils', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'com.welab.wefe.mpc.cache.intermediate.CacheOperation', 'redis.clients.jedis.Jedis', 'redis.clients.jedis.JedisPool', 'redis.clients.jedis.JedisPoolConfig'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| RedisIntermediateCache | class |  |



## 类 RedisIntermediateCache

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | RedisIntermediateCache |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| password | String |  |
| LOG = LoggerFactory.getLogger(RedisIntermediateCache.class) | Logger |  |
| jedisPool = null | JedisPool |  |
| port | int |  |
| host | String |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| get | Object |  |
| getJedisPoolInstance | JedisPool |  |
| save | void |  |
| delete | void |  |




