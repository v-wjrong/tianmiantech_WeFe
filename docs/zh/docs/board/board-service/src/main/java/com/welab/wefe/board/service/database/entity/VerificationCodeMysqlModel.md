# 基础信息

|      |      |
|------|------|
| 名称 | VerificationCodeMysqlModel |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/database/entity/VerificationCodeMysqlModel.java |
| 包名 | com.welab.wefe.board.service.database.entity |
| 依赖项 | ['com.welab.wefe.board.service.database.entity.base.AbstractMySqlModel', 'com.welab.wefe.common.verification.code.common.CaptchaSendChannel', 'com.welab.wefe.common.verification.code.common.VerificationCodeBusinessType', 'com.welab.wefe.common.web.util.DatabaseEncryptConverter', 'javax.persistence.Convert', 'javax.persistence.Entity', 'javax.persistence.EnumType', 'javax.persistence.Enumerated'] |
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
| mobile | String |  |
| businessType | VerificationCodeBusinessType |  |
| bizId | String |  |
| respContent | String |  |
| code | String |  |
| success | String |  |
| sendChannel | CaptchaSendChannel |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| setBusinessType | void |  |
| getRespContent | String |  |
| getSendChannel | CaptchaSendChannel |  |
| getBizId | String |  |
| getCode | String |  |
| setMobile | void |  |
| setSuccess | void |  |
| getBusinessType | VerificationCodeBusinessType |  |
| getSuccess | String |  |
| setCode | void |  |
| getMobile | String |  |
| setSendChannel | void |  |
| setRespContent | void |  |
| setBizId | void |  |




