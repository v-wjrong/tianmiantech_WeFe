# Basic Information

|      |      |
|------|------|
| Name | EmailService |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/EmailService.java |
| Package Name | com.welab.wefe.board.service.service |
| Dependencies | ['com.welab.wefe.board.service.database.entity.AccountMysqlModel', 'com.welab.wefe.board.service.service.account.AccountService', 'com.welab.wefe.board.service.service.globalconfig.GlobalConfigService', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.wefe.dto.global_config.MailServerModel', 'com.welab.wefe.common.wefe.enums.MessageEvent', 'org.apache.commons.collections4.CollectionUtils', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.mail.MailSendException', 'org.springframework.mail.javamail.JavaMailSenderImpl', 'org.springframework.mail.javamail.MimeMessageHelper', 'org.springframework.stereotype.Service', 'javax.mail.Address', 'javax.mail.SendFailedException', 'javax.mail.internet.MimeMessage', 'java.util.HashSet', 'java.util.List', 'java.util.Properties', 'java.util.Set'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| EmailService | class |  |



## Class EmailService

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | EmailService |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| accountService | AccountService |  |
| messageService | MessageService |  |
| MAIL_DEFAULT_ENCODING = "UTF-8" | String |  |
| MAIL_SMTP_TIMEOUT = "30000" | String |  |
| MAIL_SMTP_CONNECTION_TIMEOUT = "30000" | String |  |
| MAIL_SMTP_WRITE_TIMEOUT = "30000" | String |  |
| globalConfigService | GlobalConfigService |  |
| MAIL_SMTP_AUTH = "true" | String |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getTotalEmails | Set<String> |  |
| sendMail | Set<String> |  |
| getMailSender | JavaMailSenderImpl |  |
| sendApprovalJobNotifyMail | Set<String> |  |
| sendMail | void |  |
| saveTotalSendFailMessage | void |  |
| getInvalidAddress | Set<String> |  |




