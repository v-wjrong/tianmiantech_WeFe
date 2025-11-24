# 基础信息

|      |      |
|------|------|
| 名称 | CacheObjects |
| 编码语言 | .java |
| 代码路径 | WeFe/fusion/fusion-service/src/main/java/com/welab/wefe/data/fusion/service/service/CacheObjects.java |
| 包名 | com.welab.wefe.data.fusion.service.service |
| 依赖项 | ['com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.web.Launcher', 'com.welab.wefe.data.fusion.service.database.entity.AccountMysqlModel', 'com.welab.wefe.data.fusion.service.database.entity.BloomFilterMySqlModel', 'com.welab.wefe.data.fusion.service.database.entity.DataSetMySqlModel', 'com.welab.wefe.data.fusion.service.database.entity.PartnerMySqlModel', 'com.welab.wefe.data.fusion.service.database.repository.AccountRepository', 'com.welab.wefe.data.fusion.service.dto.entity.globalconfig.FusionConfigModel', 'com.welab.wefe.data.fusion.service.dto.entity.globalconfig.MemberInfoModel', 'com.welab.wefe.data.fusion.service.service.bloomfilter.BloomFilterService', 'com.welab.wefe.data.fusion.service.service.dataset.DataSetService', 'com.welab.wefe.data.fusion.service.service.globalconfig.GlobalConfigService', 'org.springframework.data.domain.Sort', 'java.util.ArrayList', 'java.util.LinkedHashMap', 'java.util.List'] |
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

### 方法列表

| 名称  | 类型  | 说明 |
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




