# Basic Information

|      |      |
|------|------|
| Name | MessageEntity |
| Language | .java |
| Code Path | WeFe/gateway/src/main/java/com/welab/wefe/gateway/entity/MessageEntity.java |
| Package Name | com.welab.wefe.gateway.entity |
| Dependencies | ['com.welab.wefe.common.data.mysql.entity.AbstractUniqueIDEntity', 'com.welab.wefe.common.wefe.enums.MessageEvent', 'com.welab.wefe.common.wefe.enums.MessageLevel', 'com.welab.wefe.common.wefe.enums.ProducerType', 'javax.persistence'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| MessageEntity | class |  |



## Class MessageEntity

|      |      |
|------|------|
| Access Modifier | @Table(name = "message");@Entity;public |
| Type | class |
| Name | MessageEntity |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| title | String |  |
| producer | ProducerType |  |
| createdBy | String |  |
| unread | Boolean |  |
| content | String |  |
| event | MessageEvent |  |
| level | MessageLevel |  |
| updatedBy | String |  |

### Method List

| Name  | Type  | Description |
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




