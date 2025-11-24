# Basic Information

|      |      |
|------|------|
| Name | VerificationCodeMysqlModel |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/database/entity/VerificationCodeMysqlModel.java |
| Package Name | com.welab.wefe.board.service.database.entity |
| Dependencies | ['com.welab.wefe.board.service.database.entity.base.AbstractMySqlModel', 'com.welab.wefe.common.verification.code.common.CaptchaSendChannel', 'com.welab.wefe.common.verification.code.common.VerificationCodeBusinessType', 'com.welab.wefe.common.web.util.DatabaseEncryptConverter', 'javax.persistence.Convert', 'javax.persistence.Entity', 'javax.persistence.EnumType', 'javax.persistence.Enumerated'] |
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
| mobile | String |  |
| businessType | VerificationCodeBusinessType |  |
| bizId | String |  |
| respContent | String |  |
| code | String |  |
| success | String |  |
| sendChannel | CaptchaSendChannel |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| setBusinessType | void |  |
| getRespContent | String |  |
| getSendChannel | CaptchaSendChannel |  |
| getBizId | String |  |
| getCode | String |  |
| setMobile | void |  |
| setSuccess | void |  |
| getBusinessType | VerificationCodeBusinessType |  |
| getSuccess | String |  |
| setCode | void |  |
| getMobile | String |  |
| setSendChannel | void |  |
| setRespContent | void |  |
| setBizId | void |  |




