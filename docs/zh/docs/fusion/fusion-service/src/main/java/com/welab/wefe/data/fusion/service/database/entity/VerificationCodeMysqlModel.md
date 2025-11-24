# 基础信息

|      |      |
|------|------|
| 名称 | VerificationCodeMysqlModel |
| 编码语言 | .java |
| 代码路径 | WeFe/fusion/fusion-service/src/main/java/com/welab/wefe/data/fusion/service/database/entity/VerificationCodeMysqlModel.java |
| 包名 | com.welab.wefe.data.fusion.service.database.entity |
| 依赖项 | ['com.welab.wefe.common.web.util.DatabaseEncryptConverter', 'com.welab.wefe.common.wefe.enums.VerificationCodeBusinessType', 'com.welab.wefe.common.wefe.enums.VerificationCodeSendChannel', 'javax.persistence.Convert', 'javax.persistence.Entity', 'javax.persistence.EnumType', 'javax.persistence.Enumerated'] |
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
| sendChannel | VerificationCodeSendChannel |  |
| success | String |  |
| code | String |  |
| bizId | String |  |
| businessType | VerificationCodeBusinessType |  |
| mobile | String |  |
| respContent | String |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| setBusinessType | void |  |
| setMobile | void |  |
| getSendChannel | VerificationCodeSendChannel |  |
| getRespContent | String |  |
| setSuccess | void |  |
| getMobile | String |  |
| setSendChannel | void |  |
| getSuccess | String |  |
| getBizId | String |  |
| setCode | void |  |
| getCode | String |  |
| setRespContent | void |  |
| getBusinessType | VerificationCodeBusinessType |  |
| setBizId | void |  |




