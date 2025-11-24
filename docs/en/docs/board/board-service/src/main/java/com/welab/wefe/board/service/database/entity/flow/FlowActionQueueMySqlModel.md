# Basic Information

|      |      |
|------|------|
| Name | FlowActionQueueMySqlModel |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/database/entity/flow/FlowActionQueueMySqlModel.java |
| Package Name | com.welab.wefe.board.service.database.entity.flow |
| Dependencies | ['com.welab.wefe.board.service.database.entity.base.AbstractMySqlModel', 'com.welab.wefe.common.wefe.enums.FlowActionType', 'com.welab.wefe.common.wefe.enums.ProducerType', 'javax.persistence.Entity', 'javax.persistence.EnumType', 'javax.persistence.Enumerated'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| FlowActionQueueMySqlModel | class |  |



## Class FlowActionQueueMySqlModel

|      |      |
|------|------|
| Access Modifier | @Entity(name = "flow_action_queue");public |
| Type | class |
| Name | FlowActionQueueMySqlModel |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| params | String |  |
| priority | Integer |  |
| action | FlowActionType |  |
| producer | ProducerType |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| setProducer | void |  |
| getPriority | Integer |  |
| getProducer | ProducerType |  |
| getAction | FlowActionType |  |
| setPriority | void |  |
| setAction | void |  |
| getParams | String |  |
| setParams | void |  |




