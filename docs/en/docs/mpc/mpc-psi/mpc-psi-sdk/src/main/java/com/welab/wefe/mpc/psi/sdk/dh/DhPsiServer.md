# Basic Information

|      |      |
|------|------|
| Name | DhPsiServer |
| Language | .java |
| Code Path | WeFe/mpc/mpc-psi/mpc-psi-sdk/src/main/java/com/welab/wefe/mpc/psi/sdk/dh/DhPsiServer.java |
| Package Name | com.welab.wefe.mpc.psi.sdk.dh |
| Dependencies | ['java.math.BigInteger', 'java.util.List', 'java.util.Map', 'java.util.Random', 'java.util.Set', 'java.util.concurrent.ConcurrentHashMap', 'java.util.concurrent.CopyOnWriteArrayList', 'java.util.concurrent.ExecutorService', 'java.util.concurrent.Executors', 'java.util.concurrent.TimeUnit', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'com.welab.wefe.mpc.psi.sdk.util.PartitionUtil', 'com.welab.wefe.mpc.util.DiffieHellmanUtil'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| DhPsiServer | class |  |



## Class DhPsiServer

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | DhPsiServer |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| p | BigInteger |  |
| threads = Math.max(Runtime.getRuntime().availableProcessors(), 8) | int |  |
| keySize = 1024 | int |  |
| LOG = LoggerFactory.getLogger(DhPsiServer.class) | Logger |  |
| serverPrivateD | BigInteger |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getP | BigInteger |  |
| generaterPrivateKey | BigInteger |  |
| encryptDataset | List<String> |  |
| encryptClientDatasetMap | Map<Long, String> |  |
| setP | void |  |
| getServerPrivateD | BigInteger |  |
| setServerPrivateD | void |  |




