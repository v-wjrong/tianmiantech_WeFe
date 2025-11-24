# 基础信息

|      |      |
|------|------|
| 名称 | CaptchaService |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-web/src/main/java/com/welab/wefe/common/web/service/CaptchaService.java |
| 包名 | com.welab.wefe.common.web.service |
| 依赖项 | ['com.welab.wefe.common.WeSpecCaptcha', 'com.welab.wefe.common.web.dto.Captcha', 'net.jodah.expiringmap.ExpiringMap', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.awt', 'java.util.UUID', 'java.util.concurrent.TimeUnit'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| CaptchaService | class |  |



## 类 CaptchaService

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | CaptchaService |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| captchaMap = ExpiringMap            .builder()            .expiration(60, TimeUnit.SECONDS)            .maxSize(10000)            .build() | ExpiringMap<String, String> |  |
| LOG = LoggerFactory.getLogger(CaptchaService.class) | Logger |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| get | Captcha |  |
| get | Captcha |  |
| init | void |  |
| verify | Boolean |  |




