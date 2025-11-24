# 基础信息

|      |      |
|------|------|
| 名称 | ServiceCacheConfigModel |
| 编码语言 | .java |
| 代码路径 | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/dto/globalconfig/ServiceCacheConfigModel.java |
| 包名 | com.welab.wefe.serving.service.dto.globalconfig |
| 依赖项 | ['com.welab.wefe.common.fieldvalidate.secret.MaskStrategy', 'com.welab.wefe.common.fieldvalidate.secret.Secret', 'com.welab.wefe.serving.service.dto.globalconfig.base.AbstractConfigModel', 'com.welab.wefe.serving.service.dto.globalconfig.base.ConfigGroupConstant', 'com.welab.wefe.serving.service.dto.globalconfig.base.ConfigModel'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| ServiceCacheConfigModel | class |  |



## 类 ServiceCacheConfigModel

|      |      |
|------|------|
| 访问范围 | @ConfigModel(group = ConfigGroupConstant.SERVICE_CACHE_CONFIG);public |
| 类型 | class |
| 名称 | ServiceCacheConfigModel |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| redisPassword | String |  |
| redisPort | String |  |
| redisHost | String |  |
| type | CacheType |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getType | CacheType |  |
| setRedisPassword | void |  |
| getRedisPassword | String |  |
| getRedisPort | String |  |
| setRedisHost | void |  |
| getRedisHost | String |  |
| setType | void |  |
| setRedisPort | void |  |




