# Basic Information

|      |      |
|------|------|
| Name | DhPsiClient |
| Language | .java |
| Code Path | WeFe/mpc/mpc-psi/mpc-psi-sdk/src/main/java/com/welab/wefe/mpc/psi/sdk/dh/DhPsiClient.java |
| Package Name | com.welab.wefe.mpc.psi.sdk.dh |
| Dependencies | ['java.math.BigInteger', 'java.util.List', 'java.util.Map', 'java.util.Set', 'java.util.concurrent.ConcurrentHashMap', 'java.util.concurrent.ExecutorService', 'java.util.concurrent.Executors', 'java.util.concurrent.TimeUnit', 'java.util.concurrent.atomic.AtomicLong', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'com.welab.wefe.mpc.key.DiffieHellmanKey', 'com.welab.wefe.mpc.psi.sdk.util.PartitionUtil', 'com.welab.wefe.mpc.util.DiffieHellmanUtil'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| DhPsiClient | class |  |



## Class DhPsiClient

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | DhPsiClient |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
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

### Method List

| Name  | Type  | Description |
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




