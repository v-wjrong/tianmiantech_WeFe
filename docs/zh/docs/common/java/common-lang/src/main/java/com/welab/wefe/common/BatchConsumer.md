# 基础信息

|      |      |
|------|------|
| 名称 | BatchConsumer |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-lang/src/main/java/com/welab/wefe/common/BatchConsumer.java |
| 包名 | com.welab.wefe.common |
| 依赖项 | ['org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.util.ArrayList', 'java.util.List', 'java.util.concurrent.ConcurrentLinkedQueue', 'java.util.concurrent.atomic.AtomicBoolean', 'java.util.concurrent.atomic.AtomicInteger', 'java.util.function.Consumer'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| BatchConsumer | class |  |



## 类 BatchConsumer

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | BatchConsumer |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
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

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| add | void |  |
| waitForFinishAndClose | void |  |
| startLoop | void |  |
| waitForClean | void |  |
| drainToConsume | void |  |
| close | void |  |
| setMaxBatchSize | void |  |




