# 基础信息

|      |      |
|------|------|
| 名称 | MessageEntity |
| 编码语言 | .java |
| 代码路径 | WeFe/gateway/src/main/java/com/welab/wefe/gateway/entity/MessageEntity.java |
| 包名 | com.welab.wefe.gateway.entity |
| 依赖项 | ['com.welab.wefe.common.data.mysql.entity.AbstractUniqueIDEntity', 'com.welab.wefe.common.wefe.enums.MessageEvent', 'com.welab.wefe.common.wefe.enums.MessageLevel', 'com.welab.wefe.common.wefe.enums.ProducerType', 'javax.persistence'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| MessageEntity | class |  |



## 类 MessageEntity

|      |      |
|------|------|
| 访问范围 | @Table(name = "message");@Entity;public |
| 类型 | class |
| 名称 | MessageEntity |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| title | String |  |
| producer | ProducerType |  |
| createdBy | String |  |
| unread | Boolean |  |
| content | String |  |
| event | MessageEvent |  |
| level | MessageLevel |  |
| updatedBy | String |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| setTitle | void |  |
| setCreatedBy | void |  |
| setEvent | void |  |
| getCreatedBy | String |  |
| getLevel | MessageLevel |  |
| getProducer | ProducerType |  |
| setUnread | void |  |
| getContent | String |  |
| setContent | void |  |
| getUnread | Boolean |  |
| setLevel | void |  |
| getEvent | MessageEvent |  |
| setUpdatedBy | void |  |
| getUpdatedBy | String |  |
| setProducer | void |  |
| getTitle | String |  |




