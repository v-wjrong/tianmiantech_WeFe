# 基础信息

|      |      |
|------|------|
| 名称 | AbstractActuator |
| 编码语言 | .java |
| 代码路径 | WeFe/fusion/fusion-core/src/main/java/com/welab/wefe/fusion/core/actuator/AbstractActuator.java |
| 包名 | com.welab.wefe.fusion.core.actuator |
| 依赖项 | ['com.welab.wefe.common.TimeSpan', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.fusion.core.utils.FusionThreadPool', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.util.concurrent.atomic.LongAdder', 'com.welab.wefe.common.util.ThreadUtil.sleep'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| AbstractActuator | class |  |



## 类 AbstractActuator

|      |      |
|------|------|
| 访问范围 | public abstract |
| 类型 | class |
| 名称 | AbstractActuator |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| processedCount = new LongAdder() | LongAdder |  |
| error | String |  |
| dataCount | Long |  |
| fusionCount = new LongAdder() | LongAdder |  |
| businessId | String |  |
| startTime = System.currentTimeMillis() | long |  |
| LOG = LoggerFactory.getLogger(getClass()) | Logger |  |

### 方法列表

| 名称  | 类型  | 说明 |
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




