# Basic Information

|      |      |
|------|------|
| Name | AbstractTask |
| Language | .java |
| Code Path | WeFe/fusion/fusion-service/src/main/java/com/welab/wefe/data/fusion/service/task/AbstractTask.java |
| Package Name | com.welab.wefe.data.fusion.service.task |
| Dependencies | ['com.welab.wefe.common.util.ThreadUtil.sleep', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'com.welab.wefe.common.CommonThreadPool', 'com.welab.wefe.common.TimeSpan', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.data.fusion.service.actuator.AbstractActuator', 'com.welab.wefe.data.fusion.service.actuator.rsapsi.AbstractPsiActuator', 'com.welab.wefe.data.fusion.service.enums.PSIActuatorStatus'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| AbstractTask | class |  |



## Class AbstractTask

|      |      |
|------|------|
| Access Modifier | public abstract |
| Type | class |
| Name | AbstractTask |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| businessId | String |  |
| error | String |  |
| name | String |  |
| actuator | T |  |
| maxExecuteTimeSpan = new TimeSpan(100 * 60 * 1000) | TimeSpan |  |
| LOG = LoggerFactory.getLogger(getClass()) | Logger |  |
| startTime = System.currentTimeMillis() | long |  |

### Method List

| Name  | Type  | Description |
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




