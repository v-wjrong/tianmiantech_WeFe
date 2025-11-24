# 基础信息

|      |      |
|------|------|
| 名称 | EmailService |
| 编码语言 | .java |
| 代码路径 | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/service/EmailService.java |
| 包名 | com.welab.wefe.serving.service.service |
| 依赖项 | ['com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.wefe.enums.MessageLevel', 'com.welab.wefe.common.wefe.enums.ProducerType', 'com.welab.wefe.serving.service.database.entity.AccountMySqlModel', 'com.welab.wefe.serving.service.database.entity.MessageMysqlModel', 'com.welab.wefe.serving.service.database.repository.AccountRepository', 'com.welab.wefe.serving.service.dto.globalconfig.MailServerModel', 'com.welab.wefe.serving.service.service.globalconfig.GlobalConfigService', 'org.apache.commons.collections4.CollectionUtils', 'org.apache.commons.lang3.StringUtils', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.mail.MailSendException', 'org.springframework.mail.javamail.JavaMailSenderImpl', 'org.springframework.mail.javamail.MimeMessageHelper', 'org.springframework.stereotype.Service', 'javax.mail.Address', 'javax.mail.SendFailedException', 'javax.mail.internet.MimeMessage', 'java.util.HashSet', 'java.util.List', 'java.util.Properties', 'java.util.Set'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| EmailService | class |  |



## 类 EmailService

|      |      |
|------|------|
| 访问范围 | @Service;public |
| 类型 | class |
| 名称 | EmailService |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
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

### 方法列表

| 名称  | 类型  | 说明 |
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




