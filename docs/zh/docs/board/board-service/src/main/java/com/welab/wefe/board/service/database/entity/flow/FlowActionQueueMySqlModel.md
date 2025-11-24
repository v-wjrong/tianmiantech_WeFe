# 基础信息

|      |      |
|------|------|
| 名称 | FlowActionQueueMySqlModel |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/database/entity/flow/FlowActionQueueMySqlModel.java |
| 包名 | com.welab.wefe.board.service.database.entity.flow |
| 依赖项 | ['com.welab.wefe.board.service.database.entity.base.AbstractMySqlModel', 'com.welab.wefe.common.wefe.enums.FlowActionType', 'com.welab.wefe.common.wefe.enums.ProducerType', 'javax.persistence.Entity', 'javax.persistence.EnumType', 'javax.persistence.Enumerated'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| FlowActionQueueMySqlModel | class |  |



## 类 FlowActionQueueMySqlModel

|      |      |
|------|------|
| 访问范围 | @Entity(name = "flow_action_queue");public |
| 类型 | class |
| 名称 | FlowActionQueueMySqlModel |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| params | String |  |
| priority | Integer |  |
| action | FlowActionType |  |
| producer | ProducerType |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| setProducer | void |  |
| getPriority | Integer |  |
| getProducer | ProducerType |  |
| getAction | FlowActionType |  |
| setPriority | void |  |
| setAction | void |  |
| getParams | String |  |
| setParams | void |  |




