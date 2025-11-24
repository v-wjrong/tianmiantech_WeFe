# Basic Information

|      |      |
|------|------|
| Name | CacheObjects |
| Language | .java |
| Code Path | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/service/CacheObjects.java |
| Package Name | com.welab.wefe.serving.service.service |
| Dependencies | ['com.welab.wefe.common.constant.SecretKeyType', 'com.welab.wefe.common.web.Launcher', 'com.welab.wefe.serving.service.database.entity', 'com.welab.wefe.serving.service.database.repository.AccountRepository', 'com.welab.wefe.serving.service.database.repository.PartnerRepository', 'com.welab.wefe.serving.service.database.repository.TableModelRepository', 'com.welab.wefe.serving.service.database.repository.TableServiceRepository', 'com.welab.wefe.serving.service.dto.globalconfig.IdentityInfoModel', 'com.welab.wefe.serving.service.dto.globalconfig.UnionInfoModel', 'com.welab.wefe.serving.service.enums.ServingModeEnum', 'com.welab.wefe.serving.service.service.globalconfig.GlobalConfigService', 'org.springframework.data.domain.Sort', 'java.util.LinkedHashMap', 'java.util.List'] |
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

### Method List

| Name  | Type  | Description |
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




