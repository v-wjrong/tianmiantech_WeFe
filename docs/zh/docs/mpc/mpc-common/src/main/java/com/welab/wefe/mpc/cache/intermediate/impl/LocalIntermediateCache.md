# 基础信息

|      |      |
|------|------|
| 名称 | LocalIntermediateCache |
| 编码语言 | .java |
| 代码路径 | WeFe/mpc/mpc-common/src/main/java/com/welab/wefe/mpc/cache/intermediate/impl/LocalIntermediateCache.java |
| 包名 | com.welab.wefe.mpc.cache.intermediate.impl |
| 依赖项 | ['java.util.concurrent.TimeUnit', 'com.google.common.cache.Cache', 'com.google.common.cache.CacheBuilder', 'com.welab.wefe.mpc.cache.intermediate.CacheOperation'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| LocalIntermediateCache | class |  |



## 类 LocalIntermediateCache

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | LocalIntermediateCache |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| caches = CacheBuilder.newBuilder().expireAfterAccess(5, TimeUnit.MINUTES).build() | Cache<String, Cache<String, Object>> |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| save | void |  |
| get | Object |  |
| delete | void |  |




