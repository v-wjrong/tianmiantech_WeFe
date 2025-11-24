# Basic Information

|      |      |
|------|------|
| Name | RecvTransferMetaCountDownLatchCache |
| Language | .java |
| Code Path | WeFe/gateway/src/main/java/com/welab/wefe/gateway/cache/RecvTransferMetaCountDownLatchCache.java |
| Package Name | com.welab.wefe.gateway.cache |
| Dependencies | ['java.util.concurrent.ConcurrentHashMap', 'java.util.concurrent.CountDownLatch'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| RecvTransferMetaCountDownLatchCache | class |  |



## Class RecvTransferMetaCountDownLatchCache

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | RecvTransferMetaCountDownLatchCache |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| recvTransferMetaCountDownLatchCache = new RecvTransferMetaCountDownLatchCache() | RecvTransferMetaCountDownLatchCache |  |
| dataMap = new ConcurrentHashMap<>() | ConcurrentHashMap<String, CountDownLatch> |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| closeCountDownLatch | CountDownLatch |  |
| openCountDownLatch | void |  |
| getInstance | RecvTransferMetaCountDownLatchCache |  |
| removeCountDownLatch | CountDownLatch |  |




