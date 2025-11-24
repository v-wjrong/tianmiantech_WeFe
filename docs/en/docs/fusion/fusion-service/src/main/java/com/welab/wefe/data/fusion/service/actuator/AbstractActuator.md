# Basic Information

|      |      |
|------|------|
| Name | AbstractActuator |
| Language | .java |
| Code Path | WeFe/fusion/fusion-service/src/main/java/com/welab/wefe/data/fusion/service/actuator/AbstractActuator.java |
| Package Name | com.welab.wefe.data.fusion.service.actuator |
| Dependencies | ['com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.data.fusion.service.manager.TaskResultManager', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.util.List', 'java.util.concurrent.atomic.LongAdder'] |
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
| DUMP_TABLE_EXIST = false | boolean |  |
| LOG = LoggerFactory.getLogger(getClass()) | Logger |  |
| dataCount | Integer |  |
| processedCount = new LongAdder() | LongAdder |  |
| fusionCount = new LongAdder() | LongAdder |  |
| businessId | String |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| init | void |  |
| handle | void |  |
| createTable | void |  |
| dump | void |  |




