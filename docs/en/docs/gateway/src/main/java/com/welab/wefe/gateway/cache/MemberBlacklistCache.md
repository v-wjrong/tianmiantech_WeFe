# Basic Information

|      |      |
|------|------|
| Name | MemberBlacklistCache |
| Language | .java |
| Code Path | WeFe/gateway/src/main/java/com/welab/wefe/gateway/cache/MemberBlacklistCache.java |
| Package Name | com.welab.wefe.gateway.cache |
| Dependencies | ['com.welab.wefe.gateway.GatewayServer', 'com.welab.wefe.gateway.entity.BlacklistEntity', 'com.welab.wefe.gateway.service.BlacklistService', 'org.apache.commons.collections4.CollectionUtils', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.util.ArrayList', 'java.util.HashSet', 'java.util.List', 'java.util.Set', 'java.util.concurrent.ConcurrentSkipListSet'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| MemberBlacklistCache | class |  |



## Class MemberBlacklistCache

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | MemberBlacklistCache |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| MEMBER_BLACKLIST_CACHE = new MemberBlacklistCache() | MemberBlacklistCache |  |
| BLACKLIST_SET = new ConcurrentSkipListSet<>() | ConcurrentSkipListSet<String> |  |
| LOG = LoggerFactory.getLogger(MemberBlacklistCache.class) | Logger |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getInstance | MemberBlacklistCache |  |
| isExistBlacklist | boolean |  |
| refreshCache | boolean |  |




