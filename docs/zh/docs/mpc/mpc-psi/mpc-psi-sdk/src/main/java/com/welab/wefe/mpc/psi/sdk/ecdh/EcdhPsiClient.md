# 基础信息

|      |      |
|------|------|
| 名称 | EcdhPsiClient |
| 编码语言 | .java |
| 代码路径 | WeFe/mpc/mpc-psi/mpc-psi-sdk/src/main/java/com/welab/wefe/mpc/psi/sdk/ecdh/EcdhPsiClient.java |
| 包名 | com.welab.wefe.mpc.psi.sdk.ecdh |
| 依赖项 | ['java.math.BigInteger', 'java.security.InvalidAlgorithmParameterException', 'java.security.KeyPair', 'java.security.KeyPairGenerator', 'java.security.NoSuchAlgorithmException', 'java.security.NoSuchProviderException', 'java.security.SecureRandom', 'java.security.Security', 'java.util.List', 'java.util.Map', 'java.util.Set', 'java.util.concurrent.ConcurrentHashMap', 'java.util.concurrent.ExecutorService', 'java.util.concurrent.Executors', 'java.util.concurrent.TimeUnit', 'java.util.concurrent.atomic.AtomicLong', 'org.bouncycastle.jce.ECNamedCurveTable', 'org.bouncycastle.jce.interfaces.ECPrivateKey', 'org.bouncycastle.jce.provider.BouncyCastleProvider', 'org.bouncycastle.jce.spec.ECParameterSpec', 'org.bouncycastle.math.ec.ECCurve', 'org.bouncycastle.math.ec.ECPoint', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'com.welab.wefe.mpc.psi.sdk.util.ConverterUtil', 'com.welab.wefe.mpc.psi.sdk.util.PartitionUtil'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| EcdhPsiClient | class |  |



## 类 EcdhPsiClient

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | EcdhPsiClient |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| ellipticCurve | EllipticCurve |  |
| serverDoubleEncryptedDataset | Set<ECPoint> |  |
| clientOriginalDatasetMap | Map<Long, BigInteger> |  |
| clientPrivateD | BigInteger |  |
| clientDoubleEncryptedDatasetMap | Map<Long, ECPoint> |  |
| threads = Math.max(Runtime.getRuntime().availableProcessors(), 8) | int |  |
| LOG = LoggerFactory.getLogger(EcdhPsiClient.class) | Logger |  |
| ecCurve | ECCurve |  |
| CURVE_NAME = "prime256v1" | String |  |
| idAtomicCounter | AtomicLong |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| encryptServerDataset | void |  |
| convertDoubleEncryptedClientDataset2ECPoint | void |  |
| psi | Set<String> |  |
| encryptClientOriginalDataset | Map<Long, String> |  |
| generaterPrivateKey1 | BigInteger |  |
| generaterPrivateKey | BigInteger |  |




