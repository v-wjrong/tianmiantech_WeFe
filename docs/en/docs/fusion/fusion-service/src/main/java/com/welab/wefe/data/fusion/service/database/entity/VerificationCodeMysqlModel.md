# Basic Information

|      |      |
|------|------|
| Name | VerificationCodeMysqlModel |
| Language | .java |
| Code Path | WeFe/fusion/fusion-service/src/main/java/com/welab/wefe/data/fusion/service/database/entity/VerificationCodeMysqlModel.java |
| Package Name | com.welab.wefe.data.fusion.service.database.entity |
| Dependencies | ['com.welab.wefe.common.web.util.DatabaseEncryptConverter', 'com.welab.wefe.common.wefe.enums.VerificationCodeBusinessType', 'com.welab.wefe.common.wefe.enums.VerificationCodeSendChannel', 'javax.persistence.Convert', 'javax.persistence.Entity', 'javax.persistence.EnumType', 'javax.persistence.Enumerated'] |
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
| sendChannel | VerificationCodeSendChannel |  |
| success | String |  |
| code | String |  |
| bizId | String |  |
| businessType | VerificationCodeBusinessType |  |
| mobile | String |  |
| respContent | String |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| setBusinessType | void |  |
| setMobile | void |  |
| getSendChannel | VerificationCodeSendChannel |  |
| getRespContent | String |  |
| setSuccess | void |  |
| getMobile | String |  |
| setSendChannel | void |  |
| getSuccess | String |  |
| getBizId | String |  |
| setCode | void |  |
| getCode | String |  |
| setRespContent | void |  |
| getBusinessType | VerificationCodeBusinessType |  |
| setBizId | void |  |




