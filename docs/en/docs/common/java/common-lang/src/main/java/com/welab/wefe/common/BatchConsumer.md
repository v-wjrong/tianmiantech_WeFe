# Basic Information

|      |      |
|------|------|
| Name | BatchConsumer |
| Language | .java |
| Code Path | WeFe/common/java/common-lang/src/main/java/com/welab/wefe/common/BatchConsumer.java |
| Package Name | com.welab.wefe.common |
| Dependencies | ['org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.util.ArrayList', 'java.util.List', 'java.util.concurrent.ConcurrentLinkedQueue', 'java.util.concurrent.atomic.AtomicBoolean', 'java.util.concurrent.atomic.AtomicInteger', 'java.util.function.Consumer'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| BatchConsumer | class |  |



## Class BatchConsumer

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | BatchConsumer |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| queueSize = new AtomicInteger() | AtomicInteger |  |
| maxBatchSize | int |  |
| consumer | Consumer<List<T>> |  |
| inUse = new AtomicBoolean(true) | AtomicBoolean |  |
| lastConsumeTime | long |  |
| queue = new ConcurrentLinkedQueue<>() | ConcurrentLinkedQueue<T> |  |
| LOG = LoggerFactory.getLogger(this.getClass()) | Logger |  |
| draining = false | boolean |  |
| maxDelayMs | int |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| add | void |  |
| waitForFinishAndClose | void |  |
| startLoop | void |  |
| waitForClean | void |  |
| drainToConsume | void |  |
| close | void |  |
| setMaxBatchSize | void |  |




