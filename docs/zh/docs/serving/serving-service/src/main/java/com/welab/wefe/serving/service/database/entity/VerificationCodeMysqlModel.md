# 基础信息

|      |      |
|------|------|
| 名称 | VerificationCodeMysqlModel |
| 编码语言 | .java |
| 代码路径 | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/database/entity/VerificationCodeMysqlModel.java |
| 包名 | com.welab.wefe.serving.service.database.entity |
| 依赖项 | ['com.welab.wefe.common.verification.code.common.CaptchaSendChannel', 'com.welab.wefe.common.verification.code.common.VerificationCodeBusinessType', 'javax.persistence.Entity', 'javax.persistence.EnumType', 'javax.persistence.Enumerated'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| VerificationCodeMysqlModel | class |  |



## 类 VerificationCodeMysqlModel

|      |      |
|------|------|
| 访问范围 | @Entity(name = "verification_code");public |
| 类型 | class |
| 名称 | VerificationCodeMysqlModel |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| code | String |  |
| serialVersionUID = -2617756476649365818L | long |  |
| businessType | VerificationCodeBusinessType |  |
| bizId | String |  |
| mobile | String |  |
| respContent | String |  |
| success | String |  |
| sendChannel | CaptchaSendChannel |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getSendChannel | CaptchaSendChannel |  |
| setRespContent | void |  |
| setSuccess | void |  |
| setSendChannel | void |  |
| getMobile | String |  |
| setCode | void |  |
| getRespContent | String |  |
| getSuccess | String |  |
| setMobile | void |  |
| getCode | String |  |
| setBusinessType | void |  |
| getBusinessType | VerificationCodeBusinessType |  |
| getBizId | String |  |
| setBizId | void |  |




