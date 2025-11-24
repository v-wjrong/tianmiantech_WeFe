# 基础信息

|      |      |
|------|------|
| 名称 | IdentityInfoModel |
| 编码语言 | .java |
| 代码路径 | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/dto/globalconfig/IdentityInfoModel.java |
| 包名 | com.welab.wefe.serving.service.dto.globalconfig |
| 依赖项 | ['com.welab.wefe.common.constant.SecretKeyType', 'com.welab.wefe.common.fieldvalidate.annotation.Check', 'com.welab.wefe.common.fieldvalidate.secret.MaskStrategy', 'com.welab.wefe.common.fieldvalidate.secret.Secret', 'com.welab.wefe.serving.service.dto.globalconfig.base.AbstractConfigModel', 'com.welab.wefe.serving.service.dto.globalconfig.base.ConfigGroupConstant', 'com.welab.wefe.serving.service.dto.globalconfig.base.ConfigModel'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| IdentityInfoModel | class |  |



## 类 IdentityInfoModel

|      |      |
|------|------|
| 访问范围 | @ConfigModel(group = ConfigGroupConstant.IDENTITY_INFO);public |
| 类型 | class |
| 名称 | IdentityInfoModel |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
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

### 方法列表

| 名称  | 类型  | 说明 |
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




