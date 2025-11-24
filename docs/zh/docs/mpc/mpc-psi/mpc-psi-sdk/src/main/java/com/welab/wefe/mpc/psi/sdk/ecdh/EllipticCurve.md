# 基础信息

|      |      |
|------|------|
| 名称 | EllipticCurve |
| 编码语言 | .java |
| 代码路径 | WeFe/mpc/mpc-psi/mpc-psi-sdk/src/main/java/com/welab/wefe/mpc/psi/sdk/ecdh/EllipticCurve.java |
| 包名 | com.welab.wefe.mpc.psi.sdk.ecdh |
| 依赖项 | ['java.math.BigInteger', 'java.security.MessageDigest', 'java.util.Objects', 'org.bouncycastle.jce.spec.ECParameterSpec', 'org.bouncycastle.math.ec.ECCurve', 'org.bouncycastle.math.ec.ECFieldElement', 'org.bouncycastle.math.ec.ECPoint'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| EllipticCurve | class |  |



## 类 EllipticCurve

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | EllipticCurve |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| n | BigInteger |  |
| a | BigInteger |  |
| ONE = BigInteger.valueOf(1) | BigInteger |  |
| ZERO = BigInteger.valueOf(0) | BigInteger |  |
| g | ECPoint |  |
| b | BigInteger |  |
| TWO = BigInteger.valueOf(2) | BigInteger |  |
| p | BigInteger |  |
| THREE = BigInteger.valueOf(3) | BigInteger |  |
| ecCurve | ECCurve |  |
| ecParameterSpec | ECParameterSpec |  |
| name | String |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getNameCurve | String |  |
| toString | String |  |
| multiply | ECPoint |  |
| getPFromNameCurve | String |  |
| sqrtP | BigInteger |  |
| hashToCurve | ECPoint |  |
| getEcCurve | ECCurve |  |
| byteArrayToNonNegBigInteger | BigInteger |  |
| getEcParameterSpec | ECParameterSpec |  |
| complexSqrtP | BigInteger |  |
| getN | BigInteger |  |
| findNonResidue | BigInteger |  |
| mapMessage | ECPoint |  |
| belongs | boolean |  |
| digestToBytes | byte[] |  |
| getName | String |  |




