# 基础信息

|      |      |
|------|------|
| 名称 | MessageMysqlModel |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/database/entity/MessageMysqlModel.java |
| 包名 | com.welab.wefe.board.service.database.entity |
| 依赖项 | ['com.welab.wefe.board.service.database.entity.base.AbstractBaseMySqlModel', 'com.welab.wefe.common.wefe.enums.MessageEvent', 'com.welab.wefe.common.wefe.enums.MessageLevel', 'com.welab.wefe.common.wefe.enums.ProducerType', 'javax.persistence.Entity', 'javax.persistence.EnumType', 'javax.persistence.Enumerated'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| MessageMysqlModel | class |  |



## 类 MessageMysqlModel

|      |      |
|------|------|
| 访问范围 | @Entity(name = "message");public |
| 类型 | class |
| 名称 | MessageMysqlModel |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
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

### 方法列表

| 名称  | 类型  | 说明 |
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




