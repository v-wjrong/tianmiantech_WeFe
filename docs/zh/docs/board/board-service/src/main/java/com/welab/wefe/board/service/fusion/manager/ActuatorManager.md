# 基础信息

|      |      |
|------|------|
| 名称 | ActuatorManager |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/fusion/manager/ActuatorManager.java |
| 包名 | com.welab.wefe.board.service.fusion.manager |
| 依赖项 | ['com.welab.wefe.board.service.database.entity.fusion.FusionActuatorInfoMySqlModel', 'com.welab.wefe.board.service.database.entity.fusion.FusionTaskMySqlModel', 'com.welab.wefe.board.service.database.repository.fusion.FusionActuatorInfoRepository', 'com.welab.wefe.board.service.fusion.actuator.ClientActuator', 'com.welab.wefe.board.service.fusion.actuator.psi.ServerActuator', 'com.welab.wefe.board.service.service.fusion.FusionTaskService', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.web.Launcher', 'com.welab.wefe.fusion.core.actuator.AbstractActuator', 'com.welab.wefe.fusion.core.actuator.ActuatorCache', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory'] |
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
| fusionActuatorInfoRepository | FusionActuatorInfoRepository |  |
| LOG = LoggerFactory.getLogger(ActuatorManager.class) | Logger |  |
| fusionTaskService | FusionTaskService |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getTaskInfo | JObject |  |




