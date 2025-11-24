# 基础信息

|      |      |
|------|------|
| 名称 | DhPsiServer |
| 编码语言 | .java |
| 代码路径 | WeFe/mpc/mpc-psi/mpc-psi-sdk/src/main/java/com/welab/wefe/mpc/psi/sdk/dh/DhPsiServer.java |
| 包名 | com.welab.wefe.mpc.psi.sdk.dh |
| 依赖项 | ['java.math.BigInteger', 'java.util.List', 'java.util.Map', 'java.util.Random', 'java.util.Set', 'java.util.concurrent.ConcurrentHashMap', 'java.util.concurrent.CopyOnWriteArrayList', 'java.util.concurrent.ExecutorService', 'java.util.concurrent.Executors', 'java.util.concurrent.TimeUnit', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'com.welab.wefe.mpc.psi.sdk.util.PartitionUtil', 'com.welab.wefe.mpc.util.DiffieHellmanUtil'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| DhPsiServer | class |  |



## 类 DhPsiServer

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | DhPsiServer |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| p | BigInteger |  |
| threads = Math.max(Runtime.getRuntime().availableProcessors(), 8) | int |  |
| keySize = 1024 | int |  |
| LOG = LoggerFactory.getLogger(DhPsiServer.class) | Logger |  |
| serverPrivateD | BigInteger |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getP | BigInteger |  |
| generaterPrivateKey | BigInteger |  |
| encryptDataset | List<String> |  |
| encryptClientDatasetMap | Map<Long, String> |  |
| setP | void |  |
| getServerPrivateD | BigInteger |  |
| setServerPrivateD | void |  |




