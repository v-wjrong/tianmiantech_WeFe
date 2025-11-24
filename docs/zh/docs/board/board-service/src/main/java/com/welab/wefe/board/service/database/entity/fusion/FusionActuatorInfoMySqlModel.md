# 基础信息

|      |      |
|------|------|
| 名称 | FusionActuatorInfoMySqlModel |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/database/entity/fusion/FusionActuatorInfoMySqlModel.java |
| 包名 | com.welab.wefe.board.service.database.entity.fusion |
| 依赖项 | ['com.welab.wefe.board.service.database.entity.base.AbstractBaseMySqlModel', 'com.welab.wefe.fusion.core.enums.FusionTaskStatus', 'javax.persistence.Entity', 'javax.persistence.EnumType', 'javax.persistence.Enumerated'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| FusionActuatorInfoMySqlModel | class |  |



## 类 FusionActuatorInfoMySqlModel

|      |      |
|------|------|
| 访问范围 | @Entity(name = "fusion_actuator_info");public |
| 类型 | class |
| 名称 | FusionActuatorInfoMySqlModel |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| businessId | String |  |
| type | String |  |
| status | FusionTaskStatus |  |
| progress | int |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| setStatus | void |  |
| getProgress | int |  |
| setType | void |  |
| getType | String |  |
| getStatus | FusionTaskStatus |  |
| setProgress | void |  |
| getBusinessId | String |  |
| setBusinessId | void |  |




