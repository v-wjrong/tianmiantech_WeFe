# 基础信息

|      |      |
|------|------|
| 名称 | AbstractPsiActuator |
| 编码语言 | .java |
| 代码路径 | WeFe/fusion/fusion-service/src/main/java/com/welab/wefe/data/fusion/service/actuator/rsapsi/AbstractPsiActuator.java |
| 包名 | com.welab.wefe.data.fusion.service.actuator.rsapsi |
| 依赖项 | ['com.welab.wefe.common.util.JObject', 'com.welab.wefe.data.fusion.service.actuator.AbstractActuator', 'com.welab.wefe.data.fusion.service.enums.PSIActuatorStatus', 'com.welab.wefe.data.fusion.service.manager.TaskResultManager', 'com.welab.wefe.data.fusion.service.utils.bf.BloomFilters', 'java.util.ArrayList', 'java.util.LinkedHashMap', 'java.util.List', 'java.util.Map', 'java.util.function.Function', 'java.util.stream.Collectors'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| AbstractPsiActuator | class |  |



## 类 AbstractPsiActuator

|      |      |
|------|------|
| 访问范围 | public abstract |
| 类型 | class |
| 名称 | AbstractPsiActuator |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| bf | BloomFilters |  |
| ip | String |  |
| port | int |  |
| status = PSIActuatorStatus.uninitialized | PSIActuatorStatus |  |
| fruit = new ArrayList<>() | List<JObject> |  |
| lastLogTime = System.currentTimeMillis() | long |  |
| socketTimeout = 30 * 60 * 1000 | long |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| dump | void |  |




