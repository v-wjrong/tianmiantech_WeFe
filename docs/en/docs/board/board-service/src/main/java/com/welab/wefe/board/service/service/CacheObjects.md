# Basic Information

|      |      |
|------|------|
| Name | CacheObjects |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/CacheObjects.java |
| Package Name | com.welab.wefe.board.service.service |
| Dependencies | ['com.welab.wefe.board.service.database.entity.AccountMysqlModel', 'com.welab.wefe.board.service.database.repository.AccountRepository', 'com.welab.wefe.board.service.database.repository.BlacklistRepository', 'com.welab.wefe.board.service.database.repository.data_resource.DataResourceRepository', 'com.welab.wefe.board.service.sdk.union.UnionService', 'com.welab.wefe.board.service.sdk.union.dto.MemberBaseInfo', 'com.welab.wefe.board.service.service.globalconfig.GlobalConfigService', 'com.welab.wefe.common.Convert', 'com.welab.wefe.common.constant.SecretKeyType', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.web.Launcher', 'com.welab.wefe.common.wefe.dto.global_config.MemberInfoModel', 'com.welab.wefe.common.wefe.enums.DataResourceType', 'org.springframework.data.domain.Sort', 'java.util'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| CacheObjects | class |  |



## Class CacheObjects

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | CacheObjects |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
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

### Method List

| Name  | Type  | Description |
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




