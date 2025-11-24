# 基础信息

|      |      |
|------|------|
| 名称 | AbstractVerificationCodeService |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-verification-code/src/main/java/com/welab/wefe/common/verification/code/service/AbstractVerificationCodeService.java |
| 包名 | com.welab.wefe.common.verification.code.service |
| 依赖项 | ['com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.verification.code.AbstractClient', 'com.welab.wefe.common.verification.code.AbstractResponse', 'com.welab.wefe.common.verification.code.ClientFactory', 'com.welab.wefe.common.verification.code.common.CaptchaSendChannel', 'com.welab.wefe.common.verification.code.common.VerificationCodeBusinessType', 'net.jodah.expiringmap.ExpiringMap', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.util.Map', 'java.util.concurrent.TimeUnit'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| AbstractVerificationCodeService | class |  |



## 类 AbstractVerificationCodeService

|      |      |
|------|------|
| 访问范围 | public abstract |
| 类型 | class |
| 名称 | AbstractVerificationCodeService |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| VERIFICATION_CODE_CACHE = ExpiringMap.builder()            .expiration(VALID_DURATION_MINUTES, TimeUnit.MINUTES)            .build() | ExpiringMap<String, String> |  |
| VALID_DURATION_MINUTES = 2 | int |  |
| LOG = LoggerFactory.getLogger(AbstractVerificationCodeService.class) | Logger |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| checkVerificationCode | void |  |
| send | void |  |
| buildExtendParams | Map<String, Object> |  |
| getVerificationCodeSendChannel | CaptchaSendChannel |  |
| check | void |  |
| saveSendRecord | void |  |
| generateVerificationCode | String |  |
| buildCacheKey | String |  |




