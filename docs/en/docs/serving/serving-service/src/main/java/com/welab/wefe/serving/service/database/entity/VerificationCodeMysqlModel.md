# Basic Information

|      |      |
|------|------|
| Name | VerificationCodeMysqlModel |
| Language | .java |
| Code Path | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/database/entity/VerificationCodeMysqlModel.java |
| Package Name | com.welab.wefe.serving.service.database.entity |
| Dependencies | ['com.welab.wefe.common.verification.code.common.CaptchaSendChannel', 'com.welab.wefe.common.verification.code.common.VerificationCodeBusinessType', 'javax.persistence.Entity', 'javax.persistence.EnumType', 'javax.persistence.Enumerated'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| VerificationCodeMysqlModel | class |  |



## Class VerificationCodeMysqlModel

|      |      |
|------|------|
| Access Modifier | @Entity(name = "verification_code");public |
| Type | class |
| Name | VerificationCodeMysqlModel |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| code | String |  |
| serialVersionUID = -2617756476649365818L | long |  |
| businessType | VerificationCodeBusinessType |  |
| bizId | String |  |
| mobile | String |  |
| respContent | String |  |
| success | String |  |
| sendChannel | CaptchaSendChannel |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getSendChannel | CaptchaSendChannel |  |
| setRespContent | void |  |
| setSuccess | void |  |
| setSendChannel | void |  |
| getMobile | String |  |
| setCode | void |  |
| getRespContent | String |  |
| getSuccess | String |  |
| setMobile | void |  |
| getCode | String |  |
| setBusinessType | void |  |
| getBusinessType | VerificationCodeBusinessType |  |
| getBizId | String |  |
| setBizId | void |  |




