# Basic Information

|      |      |
|------|------|
| Name | AbstractPsiActuator |
| Language | .java |
| Code Path | WeFe/fusion/fusion-service/src/main/java/com/welab/wefe/data/fusion/service/actuator/rsapsi/AbstractPsiActuator.java |
| Package Name | com.welab.wefe.data.fusion.service.actuator.rsapsi |
| Dependencies | ['com.welab.wefe.common.util.JObject', 'com.welab.wefe.data.fusion.service.actuator.AbstractActuator', 'com.welab.wefe.data.fusion.service.enums.PSIActuatorStatus', 'com.welab.wefe.data.fusion.service.manager.TaskResultManager', 'com.welab.wefe.data.fusion.service.utils.bf.BloomFilters', 'java.util.ArrayList', 'java.util.LinkedHashMap', 'java.util.List', 'java.util.Map', 'java.util.function.Function', 'java.util.stream.Collectors'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| AbstractPsiActuator | class |  |



## Class AbstractPsiActuator

|      |      |
|------|------|
| Access Modifier | public abstract |
| Type | class |
| Name | AbstractPsiActuator |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| bf | BloomFilters |  |
| ip | String |  |
| port | int |  |
| status = PSIActuatorStatus.uninitialized | PSIActuatorStatus |  |
| fruit = new ArrayList<>() | List<JObject> |  |
| lastLogTime = System.currentTimeMillis() | long |  |
| socketTimeout = 30 * 60 * 1000 | long |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| dump | void |  |




