# Basic Information

|      |      |
|------|------|
| Name | MemberInfoModel |
| Language | .java |
| Code Path | WeFe/common/java/common-wefe/src/main/java/com/welab/wefe/common/wefe/dto/global_config/MemberInfoModel.java |
| Package Name | com.welab.wefe.common.wefe.dto.global_config |
| Dependencies | ['com.welab.wefe.common.constant.SecretKeyType', 'com.welab.wefe.common.fieldvalidate.annotation.Check', 'com.welab.wefe.common.wefe.dto.global_config.base.AbstractConfigModel', 'com.welab.wefe.common.wefe.dto.global_config.base.ConfigGroupConstant', 'com.welab.wefe.common.wefe.dto.global_config.base.ConfigModel', 'com.welab.wefe.common.fieldvalidate.secret.MaskStrategy', 'com.welab.wefe.common.fieldvalidate.secret.Secret', 'java.util.UUID'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| MemberInfoModel | class |  |



## Class MemberInfoModel

|      |      |
|------|------|
| Access Modifier | @ConfigModel(group = ConfigGroupConstant.MEMBER_INFO);public |
| Type | class |
| Name | MemberInfoModel |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
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

### Method List

| Name  | Type  | Description |
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




