# 基础信息

|      |      |
|------|------|
| 名称 | DhPsiClient |
| 编码语言 | .java |
| 代码路径 | WeFe/mpc/mpc-psi/mpc-psi-sdk/src/main/java/com/welab/wefe/mpc/psi/sdk/dh/DhPsiClient.java |
| 包名 | com.welab.wefe.mpc.psi.sdk.dh |
| 依赖项 | ['java.math.BigInteger', 'java.util.List', 'java.util.Map', 'java.util.Set', 'java.util.concurrent.ConcurrentHashMap', 'java.util.concurrent.ExecutorService', 'java.util.concurrent.Executors', 'java.util.concurrent.TimeUnit', 'java.util.concurrent.atomic.AtomicLong', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'com.welab.wefe.mpc.key.DiffieHellmanKey', 'com.welab.wefe.mpc.psi.sdk.util.PartitionUtil', 'com.welab.wefe.mpc.util.DiffieHellmanUtil'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| DhPsiClient | class |  |



## 类 DhPsiClient

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | DhPsiClient |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| clientIdByServerKeys | Map<Long, String> |  |
| keySize = 1024 | int |  |
| p | BigInteger |  |
| threads = Math.max(Runtime.getRuntime().availableProcessors(), 8) | int |  |
| idAtomicCounter | AtomicLong |  |
| clientPrivateD | BigInteger |  |
| serverIdWithClientKeys | Set<String> |  |
| LOG = LoggerFactory.getLogger(DhPsiClient.class) | Logger |  |
| originalClientIds | Map<Long, String> |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| psi | Set<String> |  |
| encryptClientOriginalDataset | Map<Long, String> |  |
| encryptServerDataset | void |  |
| setServerIdWithClientKeys | void |  |
| getClientIdByServerKeys | Map<Long, String> |  |
| setClientIdByServerKeys | void |  |
| generaterPrivateKey | BigInteger |  |
| getP | BigInteger |  |
| setClientPrivateD | void |  |
| getOriginalClientIds | Map<Long, String> |  |
| setOriginalClientIds | void |  |
| setP | void |  |
| getClientPrivateD | BigInteger |  |
| getServerIdWithClientKeys | Set<String> |  |




