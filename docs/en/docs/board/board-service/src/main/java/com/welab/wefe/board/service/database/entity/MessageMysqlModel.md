# Basic Information

|      |      |
|------|------|
| Name | MessageMysqlModel |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/database/entity/MessageMysqlModel.java |
| Package Name | com.welab.wefe.board.service.database.entity |
| Dependencies | ['com.welab.wefe.board.service.database.entity.base.AbstractBaseMySqlModel', 'com.welab.wefe.common.wefe.enums.MessageEvent', 'com.welab.wefe.common.wefe.enums.MessageLevel', 'com.welab.wefe.common.wefe.enums.ProducerType', 'javax.persistence.Entity', 'javax.persistence.EnumType', 'javax.persistence.Enumerated'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| MessageMysqlModel | class |  |



## Class MessageMysqlModel

|      |      |
|------|------|
| Access Modifier | @Entity(name = "message");public |
| Type | class |
| Name | MessageMysqlModel |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| unread | Boolean |  |
| producer | ProducerType |  |
| level | MessageLevel |  |
| todoRelatedId1 | String |  |
| todoRelatedId2 | String |  |
| event | MessageEvent |  |
| title | String |  |
| todo | Boolean |  |
| todoComplete | Boolean |  |
| content | String |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| setTitle | void |  |
| getLevel | MessageLevel |  |
| setTodo | void |  |
| getTodoComplete | Boolean |  |
| getEvent | MessageEvent |  |
| setTodoRelatedId1 | void |  |
| getTodoRelatedId2 | String |  |
| setContent | void |  |
| getContent | String |  |
| getTodoRelatedId1 | String |  |
| getUnread | Boolean |  |
| getTodo | Boolean |  |
| setProducer | void |  |
| setEvent | void |  |
| getTitle | String |  |
| setUnread | void |  |
| setTodoComplete | void |  |
| setLevel | void |  |
| getProducer | ProducerType |  |
| setTodoRelatedId2 | void |  |




