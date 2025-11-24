# Basic Information

|      |      |
|------|------|
| Name | CaptchaService |
| Language | .java |
| Code Path | WeFe/common/java/common-web/src/main/java/com/welab/wefe/common/web/service/CaptchaService.java |
| Package Name | com.welab.wefe.common.web.service |
| Dependencies | ['com.welab.wefe.common.WeSpecCaptcha', 'com.welab.wefe.common.web.dto.Captcha', 'net.jodah.expiringmap.ExpiringMap', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.awt', 'java.util.UUID', 'java.util.concurrent.TimeUnit'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| CaptchaService | class |  |



## Class CaptchaService

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | CaptchaService |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| captchaMap = ExpiringMap            .builder()            .expiration(60, TimeUnit.SECONDS)            .maxSize(10000)            .build() | ExpiringMap<String, String> |  |
| LOG = LoggerFactory.getLogger(CaptchaService.class) | Logger |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| get | Captcha |  |
| get | Captcha |  |
| init | void |  |
| verify | Boolean |  |




