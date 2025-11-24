# 基础信息

|      |      |
|------|------|
| 名称 | JavaMailSender |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-verification-code/src/main/java/com/welab/wefe/common/verification/code/email/JavaMailSender.java |
| 包名 | com.welab.wefe.common.verification.code.email |
| 依赖项 | ['org.springframework.mail.javamail.JavaMailSenderImpl', 'org.springframework.mail.javamail.MimeMessageHelper', 'javax.mail.internet.MimeMessage', 'java.util.Properties'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| JavaMailSender | class |  |



## 类 JavaMailSender

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | JavaMailSender |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| MAIL_SMTP_CONNECTION_TIMEOUT = "30000" | String |  |
| MAIL_SMTP_WRITE_TIMEOUT = "30000" | String |  |
| MAIL_DEBUG = "true" | String |  |
| MAIL_SMTP_TIMEOUT = "30000" | String |  |
| MAIL_DEFAULT_ENCODING = "UTF-8" | String |  |
| javaMailSenderImpl | JavaMailSenderImpl |  |
| MAIL_SMTP_AUTH = "true" | String |  |
| MAIL_SMTP_SSL_ENABLE = "true" | String |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| setJavaMailProperties | void |  |
| sendHtmlMail | void |  |
| sendMail | void |  |
| getDefaultProperties | Properties |  |




