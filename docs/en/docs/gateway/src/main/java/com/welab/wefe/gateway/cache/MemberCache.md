# Basic Information

|      |      |
|------|------|
| Name | MemberCache |
| Language | .java |
| Code Path | WeFe/gateway/src/main/java/com/welab/wefe/gateway/cache/MemberCache.java |
| Package Name | com.welab.wefe.gateway.cache |
| Dependencies | ['com.welab.wefe.common.constant.SecretKeyType', 'com.welab.wefe.common.util.ThreadUtil', 'com.welab.wefe.gateway.GatewayServer', 'com.welab.wefe.gateway.entity.MemberEntity', 'com.welab.wefe.gateway.service.base.AbstractMemberService', 'org.apache.commons.collections4.CollectionUtils', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.util.ArrayList', 'java.util.List', 'java.util.Map', 'java.util.concurrent.ConcurrentHashMap'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| MemberCache | class |  |



## Class MemberCache

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | MemberCache |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| selfMember = null | MemberEntity |  |
| LOG = LoggerFactory.getLogger(MemberCache.class) | Logger |  |
| memberCache = new MemberCache() | MemberCache |  |
| totalMember = new ConcurrentHashMap<>() | ConcurrentHashMap<String, MemberEntity> |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| putAll | void |  |
| refreshCache | boolean |  |
| refreshTotalMemberCacheUntilComplete | boolean |  |
| refreshSelfMemberCacheUntilComplete | boolean |  |
| refreshCacheById | MemberEntity |  |
| getSelfMember | MemberEntity |  |
| put | void |  |
| get | MemberEntity |  |
| getInstance | MemberCache |  |
| refreshSelfMemberCache | boolean |  |
| setSelfMember | void |  |




