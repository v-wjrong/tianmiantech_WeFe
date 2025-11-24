# Basic Information

|      |      |
|------|------|
| Name | AbstractVerificationCodeService |
| Language | .java |
| Code Path | WeFe/common/java/common-verification-code/src/main/java/com/welab/wefe/common/verification/code/service/AbstractVerificationCodeService.java |
| Package Name | com.welab.wefe.common.verification.code.service |
| Dependencies | ['com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.verification.code.AbstractClient', 'com.welab.wefe.common.verification.code.AbstractResponse', 'com.welab.wefe.common.verification.code.ClientFactory', 'com.welab.wefe.common.verification.code.common.CaptchaSendChannel', 'com.welab.wefe.common.verification.code.common.VerificationCodeBusinessType', 'net.jodah.expiringmap.ExpiringMap', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.util.Map', 'java.util.concurrent.TimeUnit'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| AbstractVerificationCodeService | class |  |



## Class AbstractVerificationCodeService

|      |      |
|------|------|
| Access Modifier | public abstract |
| Type | class |
| Name | AbstractVerificationCodeService |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| VERIFICATION_CODE_CACHE = ExpiringMap.builder()            .expiration(VALID_DURATION_MINUTES, TimeUnit.MINUTES)            .build() | ExpiringMap<String, String> |  |
| VALID_DURATION_MINUTES = 2 | int |  |
| LOG = LoggerFactory.getLogger(AbstractVerificationCodeService.class) | Logger |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| checkVerificationCode | void |  |
| send | void |  |
| buildExtendParams | Map<String, Object> |  |
| getVerificationCodeSendChannel | CaptchaSendChannel |  |
| check | void |  |
| saveSendRecord | void |  |
| generateVerificationCode | String |  |
| buildCacheKey | String |  |




