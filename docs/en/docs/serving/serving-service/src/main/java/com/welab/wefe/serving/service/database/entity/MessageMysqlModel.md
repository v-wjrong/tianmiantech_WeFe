# Basic Information

|      |      |
|------|------|
| Name | MessageMysqlModel |
| Language | .java |
| Code Path | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/database/entity/MessageMysqlModel.java |
| Package Name | com.welab.wefe.serving.service.database.entity |
| Dependencies | ['javax.persistence.Entity', 'javax.persistence.EnumType', 'javax.persistence.Enumerated', 'com.welab.wefe.common.wefe.enums.MessageLevel', 'com.welab.wefe.common.wefe.enums.ProducerType'] |
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
| producer | ProducerType |  |
| title | String |  |
| content | String |  |
| level | MessageLevel |  |
| unread | Boolean |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| setContent | void |  |
| getTitle | String |  |
| setTitle | void |  |
| getLevel | MessageLevel |  |
| setProducer | void |  |
| setLevel | void |  |
| getUnread | Boolean |  |
| getContent | String |  |
| getProducer | ProducerType |  |
| setUnread | void |  |




