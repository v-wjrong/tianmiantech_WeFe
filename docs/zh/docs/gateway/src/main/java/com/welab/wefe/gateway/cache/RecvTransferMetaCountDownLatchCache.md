# 基础信息

|      |      |
|------|------|
| 名称 | RecvTransferMetaCountDownLatchCache |
| 编码语言 | .java |
| 代码路径 | WeFe/gateway/src/main/java/com/welab/wefe/gateway/cache/RecvTransferMetaCountDownLatchCache.java |
| 包名 | com.welab.wefe.gateway.cache |
| 依赖项 | ['java.util.concurrent.ConcurrentHashMap', 'java.util.concurrent.CountDownLatch'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| RecvTransferMetaCountDownLatchCache | class |  |



## 类 RecvTransferMetaCountDownLatchCache

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | RecvTransferMetaCountDownLatchCache |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| recvTransferMetaCountDownLatchCache = new RecvTransferMetaCountDownLatchCache() | RecvTransferMetaCountDownLatchCache |  |
| dataMap = new ConcurrentHashMap<>() | ConcurrentHashMap<String, CountDownLatch> |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| closeCountDownLatch | CountDownLatch |  |
| openCountDownLatch | void |  |
| getInstance | RecvTransferMetaCountDownLatchCache |  |
| removeCountDownLatch | CountDownLatch |  |




