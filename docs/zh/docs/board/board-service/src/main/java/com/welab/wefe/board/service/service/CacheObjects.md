# 基础信息

|      |      |
|------|------|
| 名称 | CacheObjects |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/CacheObjects.java |
| 包名 | com.welab.wefe.board.service.service |
| 依赖项 | ['com.welab.wefe.board.service.database.entity.AccountMysqlModel', 'com.welab.wefe.board.service.database.repository.AccountRepository', 'com.welab.wefe.board.service.database.repository.BlacklistRepository', 'com.welab.wefe.board.service.database.repository.data_resource.DataResourceRepository', 'com.welab.wefe.board.service.sdk.union.UnionService', 'com.welab.wefe.board.service.sdk.union.dto.MemberBaseInfo', 'com.welab.wefe.board.service.service.globalconfig.GlobalConfigService', 'com.welab.wefe.common.Convert', 'com.welab.wefe.common.constant.SecretKeyType', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.web.Launcher', 'com.welab.wefe.common.wefe.dto.global_config.MemberInfoModel', 'com.welab.wefe.common.wefe.enums.DataResourceType', 'org.springframework.data.domain.Sort', 'java.util'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| CacheObjects | class |  |



## 类 CacheObjects

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | CacheObjects |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| IMAGE_DATA_SET_TAGS = new TreeMap<>() | TreeMap<String, Integer> |  |
| SECRET_KEY_TYPE = null | SecretKeyType |  |
| ACCOUNT_ID_LIST = new ArrayList<>() | List<String> |  |
| MEMBER_NAME | String |  |
| RSA_PUBLIC_KEY | String |  |
| DATA_RESOURCE_TAGS = new TreeMap<>() | TreeMap<String, Integer> |  |
| TABLE_DATA_SET_TAGS = new TreeMap<>() | TreeMap<String, Integer> |  |
| ACCOUNT_MAP = new LinkedHashMap<>() | LinkedHashMap<String, String> |  |
| BLOOM_FILTER_TAGS = new TreeMap<>() | TreeMap<String, Integer> |  |
| LAST_REFRESH_ACCOUNT_MAP_TIME = 0 | long |  |
| MEMBER_MAP = new LinkedHashMap<>() | LinkedHashMap<String, MemberBaseInfo> |  |
| LAST_REFRESH_MEMBER_MAP_TIME = 0 | long |  |
| MEMBER_BLACKLIST = new HashSet<>() | Set<String> |  |
| RSA_PRIVATE_KEY | String |  |
| MEMBER_ID | String |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| isCurrentMemberAccount | boolean |  |
| getSecretKeyType | SecretKeyType |  |
| putAccount | void |  |
| refreshDataResourceTags | void |  |
| getRsaPublicKey | String |  |
| refreshDataResourceTags | void |  |
| getDataResourceTags | TreeMap<String, Integer> |  |
| refreshAccountMap | void |  |
| getNickname | String |  |
| getMemberId | String |  |
| isCurrentMember | boolean |  |
| getAccountIdList | List<String> |  |
| refreshMemberMap | void |  |
| getAccountMap | LinkedHashMap<String, String> |  |
| getRsaPrivateKey | String |  |
| getMemberBlackList | Set<String> |  |
| getMemberName | String |  |
| getMemberName | String |  |
| refreshMemberInfo | void |  |
| isMemberId | boolean |  |
| getMemberMap | LinkedHashMap<String, MemberBaseInfo> |  |
| refreshMemberBlacklist | void |  |




