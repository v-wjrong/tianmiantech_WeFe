# 基础信息

|      |      |
|------|------|
| 名称 | EmailClient |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-verification-code/src/main/java/com/welab/wefe/common/verification/code/email/EmailClient.java |
| 包名 | com.welab.wefe.common.verification.code.email |
| 依赖项 | ['com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.verification.code.AbstractClient', 'com.welab.wefe.common.verification.code.AbstractResponse', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.util.HashMap', 'java.util.Map'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| EmailClient | class |  |



## 类 EmailClient

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | EmailClient |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| MAIL_HOST = "mailHost" | String |  |
| SUBJECT = "subject" | String |  |
| MAIL_PORT = "mailPort" | String |  |
| CONTENT = "content" | String |  |
| TO = "to" | String |  |
| MAIL_PASSWORD = "mailPassword" | String |  |
| FROM = "from" | String |  |
| LOG = LoggerFactory.getLogger(EmailClient.class) | Logger |  |
| MAIL_USERNAME = "mailUsername" | String |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| send | AbstractResponse |  |
| buildExtendParams | Map<String, Object> |  |




