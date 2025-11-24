# Basic Information

|      |      |
|------|------|
| Name | IdentityInfoModel |
| Language | .java |
| Code Path | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/dto/globalconfig/IdentityInfoModel.java |
| Package Name | com.welab.wefe.serving.service.dto.globalconfig |
| Dependencies | ['com.welab.wefe.common.constant.SecretKeyType', 'com.welab.wefe.common.fieldvalidate.annotation.Check', 'com.welab.wefe.common.fieldvalidate.secret.MaskStrategy', 'com.welab.wefe.common.fieldvalidate.secret.Secret', 'com.welab.wefe.serving.service.dto.globalconfig.base.AbstractConfigModel', 'com.welab.wefe.serving.service.dto.globalconfig.base.ConfigGroupConstant', 'com.welab.wefe.serving.service.dto.globalconfig.base.ConfigModel'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| IdentityInfoModel | class |  |



## Class IdentityInfoModel

|      |      |
|------|------|
| Access Modifier | @ConfigModel(group = ConfigGroupConstant.IDENTITY_INFO);public |
| Type | class |
| Name | IdentityInfoModel |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| servingBaseUrl | String |  |
| rsaPublicKey | String |  |
| email | String |  |
| rsaPrivateKey | String |  |
| memberName | String |  |
| mode | String |  |
| memberId | String |  |
| secretKeyType = SecretKeyType.rsa | SecretKeyType |  |
| avatar | String |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| setAvatar | void |  |
| setServingBaseUrl | void |  |
| getSecretKeyType | SecretKeyType |  |
| getMemberId | String |  |
| setMode | void |  |
| getMemberName | String |  |
| getAvatar | String |  |
| setEmail | void |  |
| setRsaPublicKey | void |  |
| getRsaPublicKey | String |  |
| getEmail | String |  |
| setRsaPrivateKey | void |  |
| setMemberName | void |  |
| setMemberId | void |  |
| setSecretKeyType | void |  |
| getMode | String |  |
| getRsaPrivateKey | String |  |
| getServingBaseUrl | String |  |




