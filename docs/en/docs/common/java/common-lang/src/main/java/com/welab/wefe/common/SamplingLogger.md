# Basic Information

|      |      |
|------|------|
| Name | SamplingLogger |
| Language | .java |
| Code Path | WeFe/common/java/common-lang/src/main/java/com/welab/wefe/common/SamplingLogger.java |
| Package Name | com.welab.wefe.common |
| Dependencies | ['org.slf4j.Logger', 'java.util.concurrent.atomic.LongAdder'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| SamplingLogger | class |  |



## Class SamplingLogger

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | SamplingLogger |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| maxCount | long |  |
| lastPrintTime = 0 | long |  |
| lastAction | Runnable |  |
| log | Logger |  |
| maxInterval | TimeSpan |  |
| counter = new LongAdder() | LongAdder |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| of | SamplingLogger |  |
| of | SamplingLogger |  |
| of | SamplingLogger |  |
| emit | void |  |
| info | void |  |
| error | void |  |
| error | void |  |




