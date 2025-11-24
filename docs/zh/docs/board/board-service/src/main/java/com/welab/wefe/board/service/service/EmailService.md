# 基础信息

|      |      |
|------|------|
| 名称 | EmailService |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/EmailService.java |
| 包名 | com.welab.wefe.board.service.service |
| 依赖项 | ['com.welab.wefe.board.service.database.entity.AccountMysqlModel', 'com.welab.wefe.board.service.service.account.AccountService', 'com.welab.wefe.board.service.service.globalconfig.GlobalConfigService', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.wefe.dto.global_config.MailServerModel', 'com.welab.wefe.common.wefe.enums.MessageEvent', 'org.apache.commons.collections4.CollectionUtils', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.mail.MailSendException', 'org.springframework.mail.javamail.JavaMailSenderImpl', 'org.springframework.mail.javamail.MimeMessageHelper', 'org.springframework.stereotype.Service', 'javax.mail.Address', 'javax.mail.SendFailedException', 'javax.mail.internet.MimeMessage', 'java.util.HashSet', 'java.util.List', 'java.util.Properties', 'java.util.Set'] |
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
| accountService | AccountService |  |
| messageService | MessageService |  |
| MAIL_DEFAULT_ENCODING = "UTF-8" | String |  |
| MAIL_SMTP_TIMEOUT = "30000" | String |  |
| MAIL_SMTP_CONNECTION_TIMEOUT = "30000" | String |  |
| MAIL_SMTP_WRITE_TIMEOUT = "30000" | String |  |
| globalConfigService | GlobalConfigService |  |
| MAIL_SMTP_AUTH = "true" | String |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getTotalEmails | Set<String> |  |
| sendMail | Set<String> |  |
| getMailSender | JavaMailSenderImpl |  |
| sendApprovalJobNotifyMail | Set<String> |  |
| sendMail | void |  |
| saveTotalSendFailMessage | void |  |
| getInvalidAddress | Set<String> |  |




