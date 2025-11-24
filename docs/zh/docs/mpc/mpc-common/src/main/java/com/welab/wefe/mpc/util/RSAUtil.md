# 基础信息

|      |      |
|------|------|
| 名称 | RSAUtil |
| 编码语言 | .java |
| 代码路径 | WeFe/mpc/mpc-common/src/main/java/com/welab/wefe/mpc/util/RSAUtil.java |
| 包名 | com.welab.wefe.mpc.util |
| 依赖项 | ['org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'javax.crypto.Cipher', 'java.io', 'java.nio.charset.StandardCharsets', 'java.security', 'java.security.interfaces.RSAPrivateKey', 'java.security.interfaces.RSAPublicKey', 'java.security.spec.PKCS8EncodedKeySpec', 'java.security.spec.X509EncodedKeySpec', 'java.util.Base64', 'java.util.Enumeration'] |
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
| SIGN_ALGORITHM = "SHA1withRSA" | String |  |
| DECRYPT_BLOCK = 256 | int |  |
| LOGGER = LoggerFactory.getLogger(RSAUtil.class) | Logger |  |
| ENCRYPT_BLOCK = 245 | int |  |
| KEY_ALGORITHM = "RSA" | String |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getPublicKeyFromPem | RSAPublicKey |  |
| encryptByPublicKey | String |  |
| decryptByPrivateKey | byte[] |  |
| splitString | String[] |  |
| sign | String |  |
| decryptByPublicKey | byte[] |  |
| verify | boolean |  |
| sign | String |  |
| decryptByPublicKey | String |  |
| decryptLongMsgByPrivateKey | String |  |
| concat | byte[] |  |
| encryptByPrivateKey | String |  |
| encryptByPublicKey | byte[] |  |
| getPrivateKeyFromPem | RSAPrivateKey |  |
| readKeyFile | byte[] |  |
| getPublicKey | RSAPublicKey |  |
| decryptByPublicKey | String |  |
| encryptByPrivateKey | byte[] |  |
| encryptByPrivateKey | String |  |
| encryptLongMsgByPublicKey | byte[] |  |
| sign | String |  |
| splitArray | byte[][] |  |
| rsaByPrivateKey | byte[] |  |
| byte2Hex | String |  |
| generateKeyPair | RsaKeyPair |  |
| getPrivateKey | RSAPrivateKey |  |




