# 基础信息

|      |      |
|------|------|
| 名称 | MemberInfoModel |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-wefe/src/main/java/com/welab/wefe/common/wefe/dto/global_config/MemberInfoModel.java |
| 包名 | com.welab.wefe.common.wefe.dto.global_config |
| 依赖项 | ['com.welab.wefe.common.constant.SecretKeyType', 'com.welab.wefe.common.fieldvalidate.annotation.Check', 'com.welab.wefe.common.wefe.dto.global_config.base.AbstractConfigModel', 'com.welab.wefe.common.wefe.dto.global_config.base.ConfigGroupConstant', 'com.welab.wefe.common.wefe.dto.global_config.base.ConfigModel', 'com.welab.wefe.common.fieldvalidate.secret.MaskStrategy', 'com.welab.wefe.common.fieldvalidate.secret.Secret', 'java.util.UUID'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| MemberInfoModel | class |  |



## 类 MemberInfoModel

|      |      |
|------|------|
| 访问范围 | @ConfigModel(group = ConfigGroupConstant.MEMBER_INFO);public |
| 类型 | class |
| 名称 | MemberInfoModel |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| memberInitialized = false | boolean |  |
| memberEmail | String |  |
| memberHidden = false | Boolean |  |
| memberLogo | String |  |
| secretKeyType = SecretKeyType.rsa | SecretKeyType |  |
| memberId = UUID.randomUUID().toString().replaceAll("-", "") | String |  |
| memberAllowPublicDataSet | Boolean |  |
| memberGatewayTlsEnable | Boolean |  |
| rsaPrivateKey | String |  |
| memberName | String |  |
| memberGatewayUri | String |  |
| memberMobile | String |  |
| rsaPublicKey | String |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| setMemberLogo | void |  |
| getMemberEmail | String |  |
| setMemberName | void |  |
| getMemberMobile | String |  |
| getRsaPrivateKey | String |  |
| getMemberAllowPublicDataSet | Boolean |  |
| setMemberGatewayUri | void |  |
| getMemberGatewayUri | String |  |
| getSecretKeyType | SecretKeyType |  |
| setMemberMobile | void |  |
| getMemberId | String |  |
| setSecretKeyType | void |  |
| setMemberAllowPublicDataSet | void |  |
| getRsaPublicKey | String |  |
| getMemberName | String |  |
| setMemberId | void |  |
| setMemberHidden | void |  |
| setRsaPrivateKey | void |  |
| getMemberLogo | String |  |
| setRsaPublicKey | void |  |
| getMemberHidden | Boolean |  |
| setMemberEmail | void |  |
| getMemberGatewayTlsEnable | Boolean |  |
| setMemberGatewayTlsEnable | void |  |
| isMemberInitialized | boolean |  |
| setMemberInitialized | void |  |




