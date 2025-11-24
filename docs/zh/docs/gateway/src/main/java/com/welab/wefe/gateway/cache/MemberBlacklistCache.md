# 基础信息

|      |      |
|------|------|
| 名称 | MemberBlacklistCache |
| 编码语言 | .java |
| 代码路径 | WeFe/gateway/src/main/java/com/welab/wefe/gateway/cache/MemberBlacklistCache.java |
| 包名 | com.welab.wefe.gateway.cache |
| 依赖项 | ['com.welab.wefe.gateway.GatewayServer', 'com.welab.wefe.gateway.entity.BlacklistEntity', 'com.welab.wefe.gateway.service.BlacklistService', 'org.apache.commons.collections4.CollectionUtils', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.util.ArrayList', 'java.util.HashSet', 'java.util.List', 'java.util.Set', 'java.util.concurrent.ConcurrentSkipListSet'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| MemberBlacklistCache | class |  |



## 类 MemberBlacklistCache

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | MemberBlacklistCache |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| MEMBER_BLACKLIST_CACHE = new MemberBlacklistCache() | MemberBlacklistCache |  |
| BLACKLIST_SET = new ConcurrentSkipListSet<>() | ConcurrentSkipListSet<String> |  |
| LOG = LoggerFactory.getLogger(MemberBlacklistCache.class) | Logger |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getInstance | MemberBlacklistCache |  |
| isExistBlacklist | boolean |  |
| refreshCache | boolean |  |




