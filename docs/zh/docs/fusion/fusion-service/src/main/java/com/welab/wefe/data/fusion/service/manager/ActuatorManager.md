# 基础信息

|      |      |
|------|------|
| 名称 | ActuatorManager |
| 编码语言 | .java |
| 代码路径 | WeFe/fusion/fusion-service/src/main/java/com/welab/wefe/data/fusion/service/manager/ActuatorManager.java |
| 包名 | com.welab.wefe.data.fusion.service.manager |
| 依赖项 | ['java.net.InetAddress', 'java.net.UnknownHostException', 'java.util.ArrayList', 'java.util.List', 'java.util.concurrent.ConcurrentHashMap', 'org.apache.commons.lang3.StringUtils', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.web.Launcher', 'com.welab.wefe.data.fusion.service.config.Config', 'com.welab.wefe.data.fusion.service.database.entity.TaskMySqlModel', 'com.welab.wefe.data.fusion.service.enums.TaskStatus', 'com.welab.wefe.data.fusion.service.service.TaskService', 'com.welab.wefe.data.fusion.service.task.AbstractTask', 'com.welab.wefe.data.fusion.service.utils.bf.BloomFilters'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| ActuatorManager | class |  |



## 类 ActuatorManager

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | ActuatorManager |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| LOG = LoggerFactory.getLogger(ActuatorManager.class) | Logger |  |
| config | Config |  |
| taskService | TaskService |  |
| BLOOMFILTERS = new ConcurrentHashMap<>() | ConcurrentHashMap<String, BloomFilters> |  |
| ACTUATORS = new ConcurrentHashMap<>() | ConcurrentHashMap<String, AbstractTask> |  |

### 方法列表

| 名称  | 类型  | 说明 |
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




