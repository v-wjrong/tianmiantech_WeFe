# 基础信息

|      |      |
|------|------|
| 名称 | SamplingLogger |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-lang/src/main/java/com/welab/wefe/common/SamplingLogger.java |
| 包名 | com.welab.wefe.common |
| 依赖项 | ['org.slf4j.Logger', 'java.util.concurrent.atomic.LongAdder'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| SamplingLogger | class |  |



## 类 SamplingLogger

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | SamplingLogger |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| maxCount | long |  |
| lastPrintTime = 0 | long |  |
| lastAction | Runnable |  |
| log | Logger |  |
| maxInterval | TimeSpan |  |
| counter = new LongAdder() | LongAdder |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| of | SamplingLogger |  |
| of | SamplingLogger |  |
| of | SamplingLogger |  |
| emit | void |  |
| info | void |  |
| error | void |  |
| error | void |  |




