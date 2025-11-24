# 基础信息

|      |      |
|------|------|
| 名称 | PartnerMysqlModel |
| 编码语言 | .java |
| 代码路径 | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/database/entity/PartnerMysqlModel.java |
| 包名 | com.welab.wefe.serving.service.database.entity |
| 依赖项 | ['javax.persistence.Column', 'javax.persistence.Entity', 'com.welab.wefe.serving.service.enums.ClientStatusEnum'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| PartnerMysqlModel | class |  |



## 类 PartnerMysqlModel

|      |      |
|------|------|
| 访问范围 | @Entity(name = "partner");public |
| 类型 | class |
| 名称 | PartnerMysqlModel |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| status = ClientStatusEnum.NORMAL.getValue() | Integer |  |
| serialVersionUID = -2477812313658221499L | long |  |
| email | String |  |
| remark | String |  |
| name | String |  |
| servingBaseUrl | String |  |
| isUnionMember | boolean |  |
| code | String |  |
| isMe = false | boolean |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| setServingBaseUrl | void |  |
| setRemark | void |  |
| setStatus | void |  |
| getCode | String |  |
| setCode | void |  |
| getIsMe | boolean |  |
| setIsMe | void |  |
| getServingBaseUrl | String |  |
| setIsUnionMember | void |  |
| getEmail | String |  |
| setEmail | void |  |
| getIsUnionMember | boolean |  |
| getName | String |  |
| getRemark | String |  |
| setName | void |  |
| getStatus | Integer |  |




