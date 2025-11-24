# 基础信息

|      |      |
|------|------|
| 名称 | CacheObjects |
| 编码语言 | .java |
| 代码路径 | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/service/CacheObjects.java |
| 包名 | com.welab.wefe.serving.service.service |
| 依赖项 | ['com.welab.wefe.common.constant.SecretKeyType', 'com.welab.wefe.common.web.Launcher', 'com.welab.wefe.serving.service.database.entity', 'com.welab.wefe.serving.service.database.repository.AccountRepository', 'com.welab.wefe.serving.service.database.repository.PartnerRepository', 'com.welab.wefe.serving.service.database.repository.TableModelRepository', 'com.welab.wefe.serving.service.database.repository.TableServiceRepository', 'com.welab.wefe.serving.service.dto.globalconfig.IdentityInfoModel', 'com.welab.wefe.serving.service.dto.globalconfig.UnionInfoModel', 'com.welab.wefe.serving.service.enums.ServingModeEnum', 'com.welab.wefe.serving.service.service.globalconfig.GlobalConfigService', 'org.springframework.data.domain.Sort', 'java.util.LinkedHashMap', 'java.util.List'] |
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
| MODE | String |  |
| SECRET_KEY_TYPE | SecretKeyType |  |
| UNION_BASE_URL | String |  |
| RSA_PRIVATE_KEY | String |  |
| MEMBER_NAME | String |  |
| ACCOUNT_MAP = new LinkedHashMap<>() | LinkedHashMap<String, String> |  |
| RSA_PUBLIC_KEY | String |  |
| PARTNER_MAP = new LinkedHashMap<>() | LinkedHashMap<String, String> |  |
| SERVING_BASE_URL | String |  |
| SERVICE_MAP = new LinkedHashMap<>() | LinkedHashMap<String, String> |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getUnionBaseUrl | String |  |
| getPartnerName | String |  |
| getPartnerMap | LinkedHashMap<String, String> |  |
| refreshPartnerMap | void |  |
| refreshGlobalConfig | void |  |
| getSecretKeyType | SecretKeyType |  |
| getAccountMap | LinkedHashMap<String, String> |  |
| getRsaPrivateKey | String |  |
| getRsaPublicKey | String |  |
| getMODE | String |  |
| getServingBaseUrl | String |  |
| getMemberName | String |  |
| refreshAccountMap | void |  |
| getNickname | String |  |
| getMemberId | String |  |
| isUnionModel | boolean |  |
| refreshServiceMap | void |  |
| getServiceMap | LinkedHashMap<String, String> |  |
| getServiceName | String |  |
| putAccount | void |  |




