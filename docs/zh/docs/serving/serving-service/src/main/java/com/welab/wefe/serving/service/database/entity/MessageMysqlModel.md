# 基础信息

|      |      |
|------|------|
| 名称 | MessageMysqlModel |
| 编码语言 | .java |
| 代码路径 | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/database/entity/MessageMysqlModel.java |
| 包名 | com.welab.wefe.serving.service.database.entity |
| 依赖项 | ['javax.persistence.Entity', 'javax.persistence.EnumType', 'javax.persistence.Enumerated', 'com.welab.wefe.common.wefe.enums.MessageLevel', 'com.welab.wefe.common.wefe.enums.ProducerType'] |
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
| producer | ProducerType |  |
| title | String |  |
| content | String |  |
| level | MessageLevel |  |
| unread | Boolean |  |

### 方法列表

| 名称  | 类型  | 说明 |
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




