# 基础信息

|      |      |
|------|------|
| 名称 | MessageQueueEntity |
| 编码语言 | .java |
| 代码路径 | WeFe/gateway/src/main/java/com/welab/wefe/gateway/entity/MessageQueueEntity.java |
| 包名 | com.welab.wefe.gateway.entity |
| 依赖项 | ['com.welab.wefe.common.data.mysql.entity.AbstractUniqueIDEntity', 'javax.persistence.Column', 'javax.persistence.Entity', 'javax.persistence.Table'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| MessageQueueEntity | class |  |



## 类 MessageQueueEntity

|      |      |
|------|------|
| 访问范围 | @Table(name = "message_queue");@Entity;public |
| 类型 | class |
| 名称 | MessageQueueEntity |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| createdBy | String |  |
| updatedBy | String |  |
| params | String |  |
| priority | Integer |  |
| producer | String |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| setPriority | void |  |
| getPriority | Integer |  |
| getCreatedBy | String |  |
| getParams | String |  |
| getProducer | String |  |
| setProducer | void |  |
| setUpdatedBy | void |  |
| getUpdatedBy | String |  |
| setParams | void |  |
| setCreatedBy | void |  |




