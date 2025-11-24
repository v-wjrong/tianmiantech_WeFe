# Basic Information

|      |      |
|------|------|
| Name | ServiceCacheConfigModel |
| Language | .java |
| Code Path | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/dto/globalconfig/ServiceCacheConfigModel.java |
| Package Name | com.welab.wefe.serving.service.dto.globalconfig |
| Dependencies | ['com.welab.wefe.common.fieldvalidate.secret.MaskStrategy', 'com.welab.wefe.common.fieldvalidate.secret.Secret', 'com.welab.wefe.serving.service.dto.globalconfig.base.AbstractConfigModel', 'com.welab.wefe.serving.service.dto.globalconfig.base.ConfigGroupConstant', 'com.welab.wefe.serving.service.dto.globalconfig.base.ConfigModel'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| ServiceCacheConfigModel | class |  |



## Class ServiceCacheConfigModel

|      |      |
|------|------|
| Access Modifier | @ConfigModel(group = ConfigGroupConstant.SERVICE_CACHE_CONFIG);public |
| Type | class |
| Name | ServiceCacheConfigModel |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| redisPassword | String |  |
| redisPort | String |  |
| redisHost | String |  |
| type | CacheType |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getType | CacheType |  |
| setRedisPassword | void |  |
| getRedisPassword | String |  |
| getRedisPort | String |  |
| setRedisHost | void |  |
| getRedisHost | String |  |
| setType | void |  |
| setRedisPort | void |  |




