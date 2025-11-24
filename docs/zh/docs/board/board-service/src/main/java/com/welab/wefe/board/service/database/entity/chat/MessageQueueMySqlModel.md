# 基础信息

|      |      |
|------|------|
| 名称 | MessageQueueMySqlModel |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/database/entity/chat/MessageQueueMySqlModel.java |
| 包名 | com.welab.wefe.board.service.database.entity.chat |
| 依赖项 | ['com.welab.wefe.board.service.database.entity.base.AbstractMySqlModel', 'com.welab.wefe.common.wefe.enums.ProducerType', 'javax.persistence.Entity', 'javax.persistence.EnumType', 'javax.persistence.Enumerated'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| MessageQueueMySqlModel | class |  |



## 类 MessageQueueMySqlModel

|      |      |
|------|------|
| 访问范围 | @Entity(name = "message_queue");public |
| 类型 | class |
| 名称 | MessageQueueMySqlModel |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| priority | Integer |  |
| producer | ProducerType |  |
| params | String |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getParams | String |  |
| getPriority | Integer |  |
| setPriority | void |  |
| getProducer | ProducerType |  |
| setProducer | void |  |
| setParams | void |  |




