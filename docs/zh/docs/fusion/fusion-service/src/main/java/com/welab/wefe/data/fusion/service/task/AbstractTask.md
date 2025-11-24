# 基础信息

|      |      |
|------|------|
| 名称 | AbstractTask |
| 编码语言 | .java |
| 代码路径 | WeFe/fusion/fusion-service/src/main/java/com/welab/wefe/data/fusion/service/task/AbstractTask.java |
| 包名 | com.welab.wefe.data.fusion.service.task |
| 依赖项 | ['com.welab.wefe.common.util.ThreadUtil.sleep', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'com.welab.wefe.common.CommonThreadPool', 'com.welab.wefe.common.TimeSpan', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.data.fusion.service.actuator.AbstractActuator', 'com.welab.wefe.data.fusion.service.actuator.rsapsi.AbstractPsiActuator', 'com.welab.wefe.data.fusion.service.enums.PSIActuatorStatus'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| AbstractTask | class |  |



## 类 AbstractTask

|      |      |
|------|------|
| 访问范围 | public abstract |
| 类型 | class |
| 名称 | AbstractTask |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| businessId | String |  |
| error | String |  |
| name | String |  |
| actuator | T |  |
| maxExecuteTimeSpan = new TimeSpan(100 * 60 * 1000) | TimeSpan |  |
| LOG = LoggerFactory.getLogger(getClass()) | Logger |  |
| startTime = System.currentTimeMillis() | long |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getEstimatedSpend | long |  |
| setMaxExecuteTimeSpan | AbstractTask |  |
| getSpend | long |  |
| run | void |  |
| getDataCount | Integer |  |
| status | PSIActuatorStatus |  |
| postprocess | void |  |
| preprocess | void |  |
| execute | void |  |
| finish | void |  |
| progress | Integer |  |
| getFusionCount | Integer |  |
| isFinish | boolean |  |
| getProcessedCount | Integer |  |
| getBusinessId | String |  |




