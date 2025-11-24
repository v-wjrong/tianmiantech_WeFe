# Basic Information

|      |      |
|------|------|
| Name | SM4Util |
| Language | .java |
| Code Path | WeFe/common/java/common-lang/src/main/java/com/welab/wefe/common/util/SM4Util.java |
| Package Name | com.welab.wefe.common.util |
| Dependencies | ['org.apache.commons.codec.binary.Base64', 'org.apache.commons.codec.binary.Hex', 'org.bouncycastle.jce.provider.BouncyCastleProvider', 'org.bouncycastle.pqc.math.linearalgebra.ByteUtils', 'javax.crypto.Cipher', 'javax.crypto.KeyGenerator', 'javax.crypto.spec.IvParameterSpec', 'javax.crypto.spec.SecretKeySpec', 'java.security.AlgorithmParameters', 'java.security.Key', 'java.security.SecureRandom', 'java.security.Security', 'java.util.Arrays'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| SM4Util | class |  |



## Class SM4Util

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | SM4Util |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| DEFAULT_KEY_SIZE = 128 | int |  |
| ALGORITHM_NAME_CBC_PADDING = "SM4/CBC/PKCS5Padding" | String |  |
| ALGORITHM_NAME = "SM4" | String |  |
| ENCODING = "UTF-8" | String |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| generateIV | AlgorithmParameters |  |
| encrypt | String |  |
| generateKey | byte[] |  |
| decrypt | String |  |
| encryptCbcPadding | byte[] |  |
| generateCbcCipher | Cipher |  |
| generateKeyString | String |  |
| decryptCbcPadding | byte[] |  |
| decryptBase64 | String |  |
| encryptBase64 | String |  |




