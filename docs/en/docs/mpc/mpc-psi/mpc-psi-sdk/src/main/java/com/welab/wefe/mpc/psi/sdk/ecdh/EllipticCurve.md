# Basic Information

|      |      |
|------|------|
| Name | EllipticCurve |
| Language | .java |
| Code Path | WeFe/mpc/mpc-psi/mpc-psi-sdk/src/main/java/com/welab/wefe/mpc/psi/sdk/ecdh/EllipticCurve.java |
| Package Name | com.welab.wefe.mpc.psi.sdk.ecdh |
| Dependencies | ['java.math.BigInteger', 'java.security.MessageDigest', 'java.util.Objects', 'org.bouncycastle.jce.spec.ECParameterSpec', 'org.bouncycastle.math.ec.ECCurve', 'org.bouncycastle.math.ec.ECFieldElement', 'org.bouncycastle.math.ec.ECPoint'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| EllipticCurve | class |  |



## Class EllipticCurve

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | EllipticCurve |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
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

### Method List

| Name  | Type  | Description |
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




