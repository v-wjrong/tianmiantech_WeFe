# Basic Information

|      |      |
|------|------|
| Name | JavaMailSender |
| Language | .java |
| Code Path | WeFe/common/java/common-verification-code/src/main/java/com/welab/wefe/common/verification/code/email/JavaMailSender.java |
| Package Name | com.welab.wefe.common.verification.code.email |
| Dependencies | ['org.springframework.mail.javamail.JavaMailSenderImpl', 'org.springframework.mail.javamail.MimeMessageHelper', 'javax.mail.internet.MimeMessage', 'java.util.Properties'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| JavaMailSender | class |  |



## Class JavaMailSender

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | JavaMailSender |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| MAIL_SMTP_CONNECTION_TIMEOUT = "30000" | String |  |
| MAIL_SMTP_WRITE_TIMEOUT = "30000" | String |  |
| MAIL_DEBUG = "true" | String |  |
| MAIL_SMTP_TIMEOUT = "30000" | String |  |
| MAIL_DEFAULT_ENCODING = "UTF-8" | String |  |
| javaMailSenderImpl | JavaMailSenderImpl |  |
| MAIL_SMTP_AUTH = "true" | String |  |
| MAIL_SMTP_SSL_ENABLE = "true" | String |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| setJavaMailProperties | void |  |
| sendHtmlMail | void |  |
| sendMail | void |  |
| getDefaultProperties | Properties |  |




