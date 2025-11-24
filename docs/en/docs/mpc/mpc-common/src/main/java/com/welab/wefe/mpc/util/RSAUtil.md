# Basic Information

|      |      |
|------|------|
| Name | RSAUtil |
| Language | .java |
| Code Path | WeFe/mpc/mpc-common/src/main/java/com/welab/wefe/mpc/util/RSAUtil.java |
| Package Name | com.welab.wefe.mpc.util |
| Dependencies | ['org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'javax.crypto.Cipher', 'java.io', 'java.nio.charset.StandardCharsets', 'java.security', 'java.security.interfaces.RSAPrivateKey', 'java.security.interfaces.RSAPublicKey', 'java.security.spec.PKCS8EncodedKeySpec', 'java.security.spec.X509EncodedKeySpec', 'java.util.Base64', 'java.util.Enumeration'] |
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
| SIGN_ALGORITHM = "SHA1withRSA" | String |  |
| DECRYPT_BLOCK = 256 | int |  |
| LOGGER = LoggerFactory.getLogger(RSAUtil.class) | Logger |  |
| ENCRYPT_BLOCK = 245 | int |  |
| KEY_ALGORITHM = "RSA" | String |  |

### Method List

| Name  | Type  | Description |
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




