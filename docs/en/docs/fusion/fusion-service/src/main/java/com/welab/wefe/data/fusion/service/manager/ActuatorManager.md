# Basic Information

|      |      |
|------|------|
| Name | ActuatorManager |
| Language | .java |
| Code Path | WeFe/fusion/fusion-service/src/main/java/com/welab/wefe/data/fusion/service/manager/ActuatorManager.java |
| Package Name | com.welab.wefe.data.fusion.service.manager |
| Dependencies | ['java.net.InetAddress', 'java.net.UnknownHostException', 'java.util.ArrayList', 'java.util.List', 'java.util.concurrent.ConcurrentHashMap', 'org.apache.commons.lang3.StringUtils', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.web.Launcher', 'com.welab.wefe.data.fusion.service.config.Config', 'com.welab.wefe.data.fusion.service.database.entity.TaskMySqlModel', 'com.welab.wefe.data.fusion.service.enums.TaskStatus', 'com.welab.wefe.data.fusion.service.service.TaskService', 'com.welab.wefe.data.fusion.service.task.AbstractTask', 'com.welab.wefe.data.fusion.service.utils.bf.BloomFilters'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| ActuatorManager | class |  |



## Class ActuatorManager

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | ActuatorManager |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| LOG = LoggerFactory.getLogger(ActuatorManager.class) | Logger |  |
| config | Config |  |
| taskService | TaskService |  |
| BLOOMFILTERS = new ConcurrentHashMap<>() | ConcurrentHashMap<String, BloomFilters> |  |
| ACTUATORS = new ConcurrentHashMap<>() | ConcurrentHashMap<String, AbstractTask> |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| setBloomFilters | void |  |
| size | int |  |
| getTaskInfo | JObject |  |
| set | void |  |
| remove | void |  |
| get | AbstractTask |  |
| ip | String |  |
| dashboard | List<JObject> |  |
| getBloomFilters | BloomFilters |  |




