# 基础信息

|      |      |
|------|------|
| 名称 | SM4Util |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-lang/src/main/java/com/welab/wefe/common/util/SM4Util.java |
| 包名 | com.welab.wefe.common.util |
| 依赖项 | ['org.apache.commons.codec.binary.Base64', 'org.apache.commons.codec.binary.Hex', 'org.bouncycastle.jce.provider.BouncyCastleProvider', 'org.bouncycastle.pqc.math.linearalgebra.ByteUtils', 'javax.crypto.Cipher', 'javax.crypto.KeyGenerator', 'javax.crypto.spec.IvParameterSpec', 'javax.crypto.spec.SecretKeySpec', 'java.security.AlgorithmParameters', 'java.security.Key', 'java.security.SecureRandom', 'java.security.Security', 'java.util.Arrays'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| SM4Util | class |  |



## 类 SM4Util

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | SM4Util |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| DEFAULT_KEY_SIZE = 128 | int |  |
| ALGORITHM_NAME_CBC_PADDING = "SM4/CBC/PKCS5Padding" | String |  |
| ALGORITHM_NAME = "SM4" | String |  |
| ENCODING = "UTF-8" | String |  |

### 方法列表

| 名称  | 类型  | 说明 |
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




