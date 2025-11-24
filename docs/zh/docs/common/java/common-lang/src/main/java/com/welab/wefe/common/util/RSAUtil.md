# 基础信息

|      |      |
|------|------|
| 名称 | RSAUtil |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-lang/src/main/java/com/welab/wefe/common/util/RSAUtil.java |
| 包名 | com.welab.wefe.common.util |
| 依赖项 | ['com.alibaba.fastjson.JSON', 'org.apache.commons.codec.binary.Base64', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.util.Base64Utils', 'javax.crypto.Cipher', 'java.io', 'java.nio.charset.StandardCharsets', 'java.security', 'java.security.interfaces.RSAPrivateKey', 'java.security.interfaces.RSAPublicKey', 'java.security.spec.PKCS8EncodedKeySpec', 'java.security.spec.X509EncodedKeySpec', 'java.util.Enumeration'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| RSAUtil | class |  |



## 类 RSAUtil

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | RSAUtil |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| LOG = LoggerFactory.getLogger(RSAUtil.class) | Logger |  |
| DECRYPT_BLOCK = 256 | int |  |
| KEY_ALGORITHM = "RSA" | String |  |
| SIGN_ALGORITHM = "SHA1withRSA" | String |  |
| ENCRYPT_BLOCK = 245 | int |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| byte2Hex | String |  |
| generateKeyPair | RsaKeyPair |  |
| main | void |  |
| decryptByPrivateKey | byte[] |  |
| sign | String |  |
| decryptByPublicKey | byte[] |  |
| concat | byte[] |  |
| decryptByPublicKey | String |  |
| sign | String |  |
| getPublicKeyFromPem | RSAPublicKey |  |
| verify | boolean |  |
| decryptLongMsgByPrivateKey | String |  |
| readKeyFile | byte[] |  |
| decryptByPrivateKey | String |  |
| getPrivateKeyFromPem | RSAPrivateKey |  |
| encryptByPrivateKey | byte[] |  |
| decryptByPublicKey | String |  |
| getPrivateKey | RSAPrivateKey |  |
| encryptByPublicKey | String |  |
| encryptLongMsgByPublicKey | byte[] |  |
| encryptByPublicKey | byte[] |  |
| sign | String |  |
| getPublicKey | RSAPublicKey |  |
| encryptByPrivateKey | String |  |
| encryptByPrivateKey | String |  |
| splitString | String[] |  |
| splitArray | byte[][] |  |
| rsaByPrivateKey | byte[] |  |




