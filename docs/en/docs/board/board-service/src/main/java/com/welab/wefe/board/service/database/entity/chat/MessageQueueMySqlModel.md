# Basic Information

|      |      |
|------|------|
| Name | MessageQueueMySqlModel |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/database/entity/chat/MessageQueueMySqlModel.java |
| Package Name | com.welab.wefe.board.service.database.entity.chat |
| Dependencies | ['com.welab.wefe.board.service.database.entity.base.AbstractMySqlModel', 'com.welab.wefe.common.wefe.enums.ProducerType', 'javax.persistence.Entity', 'javax.persistence.EnumType', 'javax.persistence.Enumerated'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| MessageQueueMySqlModel | class |  |



## Class MessageQueueMySqlModel

|      |      |
|------|------|
| Access Modifier | @Entity(name = "message_queue");public |
| Type | class |
| Name | MessageQueueMySqlModel |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| priority | Integer |  |
| producer | ProducerType |  |
| params | String |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getParams | String |  |
| getPriority | Integer |  |
| setPriority | void |  |
| getProducer | ProducerType |  |
| setProducer | void |  |
| setParams | void |  |




