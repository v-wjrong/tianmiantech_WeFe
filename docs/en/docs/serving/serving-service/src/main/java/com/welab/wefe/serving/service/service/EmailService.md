# Basic Information

|      |      |
|------|------|
| Name | EmailService |
| Language | .java |
| Code Path | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/service/EmailService.java |
| Package Name | com.welab.wefe.serving.service.service |
| Dependencies | ['com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.wefe.enums.MessageLevel', 'com.welab.wefe.common.wefe.enums.ProducerType', 'com.welab.wefe.serving.service.database.entity.AccountMySqlModel', 'com.welab.wefe.serving.service.database.entity.MessageMysqlModel', 'com.welab.wefe.serving.service.database.repository.AccountRepository', 'com.welab.wefe.serving.service.dto.globalconfig.MailServerModel', 'com.welab.wefe.serving.service.service.globalconfig.GlobalConfigService', 'org.apache.commons.collections4.CollectionUtils', 'org.apache.commons.lang3.StringUtils', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.mail.MailSendException', 'org.springframework.mail.javamail.JavaMailSenderImpl', 'org.springframework.mail.javamail.MimeMessageHelper', 'org.springframework.stereotype.Service', 'javax.mail.Address', 'javax.mail.SendFailedException', 'javax.mail.internet.MimeMessage', 'java.util.HashSet', 'java.util.List', 'java.util.Properties', 'java.util.Set'] |
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
| MAIL_SMTP_TIMEOUT = "30000" | String |  |
| LOG = LoggerFactory.getLogger(this.getClass()) | Logger |  |
| accountRepository | AccountRepository |  |
| MAIL_SMTP_WRITE_TIMEOUT = "30000" | String |  |
| MAIL_SMTP_AUTH = "true" | String |  |
| messageService | MessageService |  |
| MAIL_DEFAULT_ENCODING = "UTF-8" | String |  |
| configService | GlobalConfigService |  |
| MAIL_SMTP_CONNECTION_TIMEOUT = "30000" | String |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getTotalEmails | Set<String> |  |
| sendMail | void |  |
| sendApprovalJobNotifyMail | Set<String> |  |
| sendMail | Set<String> |  |
| getMailSender | JavaMailSenderImpl |  |
| saveTotalSendFailMessage | void |  |
| savePartSendFailMessage | void |  |
| saveErrorMessage | void |  |
| getInvalidAddress | Set<String> |  |




