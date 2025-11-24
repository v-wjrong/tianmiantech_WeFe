# Basic Information

|      |      |
|------|------|
| Name | AbstractActuator |
| Language | .java |
| Code Path | WeFe/fusion/fusion-core/src/main/java/com/welab/wefe/fusion/core/actuator/AbstractActuator.java |
| Package Name | com.welab.wefe.fusion.core.actuator |
| Dependencies | ['com.welab.wefe.common.TimeSpan', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.fusion.core.utils.FusionThreadPool', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.util.concurrent.atomic.LongAdder', 'com.welab.wefe.common.util.ThreadUtil.sleep'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| AbstractActuator | class |  |



## Class AbstractActuator

|      |      |
|------|------|
| Access Modifier | public abstract |
| Type | class |
| Name | AbstractActuator |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| processedCount = new LongAdder() | LongAdder |  |
| error | String |  |
| dataCount | Long |  |
| fusionCount = new LongAdder() | LongAdder |  |
| businessId | String |  |
| startTime = System.currentTimeMillis() | long |  |
| LOG = LoggerFactory.getLogger(getClass()) | Logger |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| isFinish | boolean |  |
| fusion | void |  |
| run | void |  |
| getBusinessId | String |  |
| execute | void |  |
| getFusionCount | long |  |
| heartbeat | void |  |
| getEstimatedSpend | long |  |
| progress | int |  |
| setMaxExecuteTimeSpan | AbstractActuator |  |
| getDataCount | long |  |
| getProcessedCount | long |  |
| getSpend | long |  |




