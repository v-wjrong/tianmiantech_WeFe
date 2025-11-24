# Basic Information

|      |      |
|------|------|
| Name | VerificationCodeService |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/verificationcode/VerificationCodeService.java |
| Package Name | com.welab.wefe.board.service.service.verificationcode |
| Dependencies | ['com.welab.wefe.board.service.constant.Config', 'com.welab.wefe.board.service.database.entity.AccountMysqlModel', 'com.welab.wefe.board.service.database.entity.VerificationCodeMysqlModel', 'com.welab.wefe.board.service.database.repository.AccountRepository', 'com.welab.wefe.board.service.database.repository.VerificationCodeRepository', 'com.welab.wefe.board.service.service.globalconfig.GlobalConfigService', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.verification.code.AbstractResponse', 'com.welab.wefe.common.verification.code.common.CaptchaSendChannel', 'com.welab.wefe.common.verification.code.common.VerificationCodeBusinessType', 'com.welab.wefe.common.verification.code.email.EmailClient', 'com.welab.wefe.common.verification.code.service.AbstractVerificationCodeService', 'com.welab.wefe.common.verification.code.sms.AliyunSmsClient', 'com.welab.wefe.common.web.util.DatabaseEncryptUtil', 'com.welab.wefe.common.wefe.dto.global_config.AlertConfigModel', 'com.welab.wefe.common.wefe.dto.global_config.AliyunSmsChannelConfigModel', 'com.welab.wefe.common.wefe.dto.global_config.MailServerModel', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.stereotype.Service', 'java.util.Map', 'java.util.UUID'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| VerificationCodeService | class |  |



## Class VerificationCodeService

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | VerificationCodeService |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| verificationCodeRepository | VerificationCodeRepository |  |
| accountRepository | AccountRepository |  |
| globalConfigService | GlobalConfigService |  |
| LOG = LoggerFactory.getLogger(VerificationCodeService.class) | Logger |  |
| config | Config |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| check | void |  |
| buildExtendParams | Map<String, Object> |  |
| saveSendRecord | void |  |
| getVerificationCodeSendChannel | CaptchaSendChannel |  |
| checkEmailConfig | void |  |
| checkSmsConfig | void |  |




