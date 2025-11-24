# Basic Information

|      |      |
|------|------|
| Name | RSAUtil |
| Language | .java |
| Code Path | WeFe/common/java/common-lang/src/main/java/com/welab/wefe/common/util/RSAUtil.java |
| Package Name | com.welab.wefe.common.util |
| Dependencies | ['com.alibaba.fastjson.JSON', 'org.apache.commons.codec.binary.Base64', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.util.Base64Utils', 'javax.crypto.Cipher', 'java.io', 'java.nio.charset.StandardCharsets', 'java.security', 'java.security.interfaces.RSAPrivateKey', 'java.security.interfaces.RSAPublicKey', 'java.security.spec.PKCS8EncodedKeySpec', 'java.security.spec.X509EncodedKeySpec', 'java.util.Enumeration'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| RSAUtil | class |  |



## Class RSAUtil

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | RSAUtil |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| LOG = LoggerFactory.getLogger(RSAUtil.class) | Logger |  |
| DECRYPT_BLOCK = 256 | int |  |
| KEY_ALGORITHM = "RSA" | String |  |
| SIGN_ALGORITHM = "SHA1withRSA" | String |  |
| ENCRYPT_BLOCK = 245 | int |  |

### Method List

| Name  | Type  | Description |
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




