# Basic Information

|      |      |
|------|------|
| Name | CacheObjects |
| Language | .java |
| Code Path | WeFe/fusion/fusion-service/src/main/java/com/welab/wefe/data/fusion/service/service/CacheObjects.java |
| Package Name | com.welab.wefe.data.fusion.service.service |
| Dependencies | ['com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.web.Launcher', 'com.welab.wefe.data.fusion.service.database.entity.AccountMysqlModel', 'com.welab.wefe.data.fusion.service.database.entity.BloomFilterMySqlModel', 'com.welab.wefe.data.fusion.service.database.entity.DataSetMySqlModel', 'com.welab.wefe.data.fusion.service.database.entity.PartnerMySqlModel', 'com.welab.wefe.data.fusion.service.database.repository.AccountRepository', 'com.welab.wefe.data.fusion.service.dto.entity.globalconfig.FusionConfigModel', 'com.welab.wefe.data.fusion.service.dto.entity.globalconfig.MemberInfoModel', 'com.welab.wefe.data.fusion.service.service.bloomfilter.BloomFilterService', 'com.welab.wefe.data.fusion.service.service.dataset.DataSetService', 'com.welab.wefe.data.fusion.service.service.globalconfig.GlobalConfigService', 'org.springframework.data.domain.Sort', 'java.util.ArrayList', 'java.util.LinkedHashMap', 'java.util.List'] |
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
| MEMBER_ID | String |  |
| BLOOM_FILTER_MAP = new LinkedHashMap<>() | LinkedHashMap<String, String> |  |
| RSA_PRIVATE_KEY | String |  |
| DATA_SET_MAP = new LinkedHashMap<>() | LinkedHashMap<String, String> |  |
| ACCOUNT_ID_LIST = new ArrayList<>() | List<String> |  |
| PARTNER_MAP = new LinkedHashMap<>() | LinkedHashMap<String, String> |  |
| RSA_PUBLIC_KEY | String |  |
| ACCOUNT_MAP = new LinkedHashMap<>() | LinkedHashMap<String, String> |  |
| OPEN_SOCKET_PORT | Integer |  |
| MEMBER_NAME | String |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getPartnerMap | LinkedHashMap<String, String> |  |
| getAccountIdList | List<String> |  |
| getMemberId | String |  |
| getDataSetMap | LinkedHashMap<String, String> |  |
| getMemberName | String |  |
| getDataSetName | String |  |
| getAccountMap | LinkedHashMap<String, String> |  |
| isCurrentMember | boolean |  |
| refreshDataSetMap | void |  |
| getOpenSocketPort | Integer |  |
| getRsaPrivateKey | String |  |
| getPartnerName | String |  |
| getBloomFilterMap | LinkedHashMap<String, String> |  |
| getBloomFilterName | String |  |
| refreshPartnerMap | void |  |
| getRsaPublicKey | String |  |
| getNickname | String |  |
| isCurrentMemberAccount | boolean |  |
| refreshMemberInfo | void |  |
| refreshFusionConfig | void |  |
| refreshAccountMap | void |  |
| putAccount | void |  |
| refreshBloomFilterMap | void |  |




