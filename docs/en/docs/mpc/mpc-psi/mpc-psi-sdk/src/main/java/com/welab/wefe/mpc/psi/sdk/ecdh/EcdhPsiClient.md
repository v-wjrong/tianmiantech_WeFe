# Basic Information

|      |      |
|------|------|
| Name | EcdhPsiClient |
| Language | .java |
| Code Path | WeFe/mpc/mpc-psi/mpc-psi-sdk/src/main/java/com/welab/wefe/mpc/psi/sdk/ecdh/EcdhPsiClient.java |
| Package Name | com.welab.wefe.mpc.psi.sdk.ecdh |
| Dependencies | ['java.math.BigInteger', 'java.security.InvalidAlgorithmParameterException', 'java.security.KeyPair', 'java.security.KeyPairGenerator', 'java.security.NoSuchAlgorithmException', 'java.security.NoSuchProviderException', 'java.security.SecureRandom', 'java.security.Security', 'java.util.List', 'java.util.Map', 'java.util.Set', 'java.util.concurrent.ConcurrentHashMap', 'java.util.concurrent.ExecutorService', 'java.util.concurrent.Executors', 'java.util.concurrent.TimeUnit', 'java.util.concurrent.atomic.AtomicLong', 'org.bouncycastle.jce.ECNamedCurveTable', 'org.bouncycastle.jce.interfaces.ECPrivateKey', 'org.bouncycastle.jce.provider.BouncyCastleProvider', 'org.bouncycastle.jce.spec.ECParameterSpec', 'org.bouncycastle.math.ec.ECCurve', 'org.bouncycastle.math.ec.ECPoint', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'com.welab.wefe.mpc.psi.sdk.util.ConverterUtil', 'com.welab.wefe.mpc.psi.sdk.util.PartitionUtil'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| EcdhPsiClient | class |  |



## Class EcdhPsiClient

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | EcdhPsiClient |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
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

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| encryptServerDataset | void |  |
| convertDoubleEncryptedClientDataset2ECPoint | void |  |
| psi | Set<String> |  |
| encryptClientOriginalDataset | Map<Long, String> |  |
| generaterPrivateKey1 | BigInteger |  |
| generaterPrivateKey | BigInteger |  |




