# 基础信息

|      |      |
|------|------|
| 名称 | MemberCache |
| 编码语言 | .java |
| 代码路径 | WeFe/gateway/src/main/java/com/welab/wefe/gateway/cache/MemberCache.java |
| 包名 | com.welab.wefe.gateway.cache |
| 依赖项 | ['com.welab.wefe.common.constant.SecretKeyType', 'com.welab.wefe.common.util.ThreadUtil', 'com.welab.wefe.gateway.GatewayServer', 'com.welab.wefe.gateway.entity.MemberEntity', 'com.welab.wefe.gateway.service.base.AbstractMemberService', 'org.apache.commons.collections4.CollectionUtils', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.util.ArrayList', 'java.util.List', 'java.util.Map', 'java.util.concurrent.ConcurrentHashMap'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| MemberCache | class |  |



## 类 MemberCache

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | MemberCache |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| selfMember = null | MemberEntity |  |
| LOG = LoggerFactory.getLogger(MemberCache.class) | Logger |  |
| memberCache = new MemberCache() | MemberCache |  |
| totalMember = new ConcurrentHashMap<>() | ConcurrentHashMap<String, MemberEntity> |  |

### 方法列表

| 名称  | 类型  | 说明 |
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




