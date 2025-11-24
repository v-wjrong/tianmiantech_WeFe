# 基础信息

|      |      |
|------|------|
| 名称 | AESUtil |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-lang/src/main/java/com/welab/wefe/common/util/AESUtil.java |
| 包名 | com.welab.wefe.common.util |
| 依赖项 | ['com.welab.wefe.common.constant.Constant', 'org.apache.commons.codec.binary.Base64', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'javax.crypto.Cipher', 'javax.crypto.KeyGenerator', 'javax.crypto.spec.IvParameterSpec', 'javax.crypto.spec.SecretKeySpec', 'java.io.IOException', 'java.io.UnsupportedEncodingException', 'java.security.Key', 'java.security.SecureRandom'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| AESUtil | class |  |



## 类 AESUtil

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | AESUtil |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| AESTYPE = "AES/ECB/PKCS5Padding" | String |  |
| LOG = LoggerFactory.getLogger(AESUtil.class) | Logger |  |
| AES2 = "AES2" | String |  |
| AES_CBC_NO_PADDING = "AES/CBC/NoPadding" | String |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| decrypt | byte[] |  |
| encrypt | String |  |
| encrypt | byte[] |  |
| aesSecure2 | byte[] |  |
| decrypt | byte[] |  |
| encrypt | byte[] |  |
| decrypt | String |  |
| decrypt | String |  |
| encrypt | String |  |
| aesSecure | byte[] |  |
| aesSecureWithViParam | String |  |
| generateKey | Key |  |




