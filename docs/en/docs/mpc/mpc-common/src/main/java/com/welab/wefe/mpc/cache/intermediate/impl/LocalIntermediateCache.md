# Basic Information

|      |      |
|------|------|
| Name | LocalIntermediateCache |
| Language | .java |
| Code Path | WeFe/mpc/mpc-common/src/main/java/com/welab/wefe/mpc/cache/intermediate/impl/LocalIntermediateCache.java |
| Package Name | com.welab.wefe.mpc.cache.intermediate.impl |
| Dependencies | ['java.util.concurrent.TimeUnit', 'com.google.common.cache.Cache', 'com.google.common.cache.CacheBuilder', 'com.welab.wefe.mpc.cache.intermediate.CacheOperation'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| LocalIntermediateCache | class |  |



## Class LocalIntermediateCache

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | LocalIntermediateCache |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| caches = CacheBuilder.newBuilder().expireAfterAccess(5, TimeUnit.MINUTES).build() | Cache<String, Cache<String, Object>> |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| save | void |  |
| get | Object |  |
| delete | void |  |




