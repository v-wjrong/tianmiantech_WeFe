# Basic Information

|      |      |
|------|------|
| Name | PartnerMysqlModel |
| Language | .java |
| Code Path | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/database/entity/PartnerMysqlModel.java |
| Package Name | com.welab.wefe.serving.service.database.entity |
| Dependencies | ['javax.persistence.Column', 'javax.persistence.Entity', 'com.welab.wefe.serving.service.enums.ClientStatusEnum'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| PartnerMysqlModel | class |  |



## Class PartnerMysqlModel

|      |      |
|------|------|
| Access Modifier | @Entity(name = "partner");public |
| Type | class |
| Name | PartnerMysqlModel |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
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

### Method List

| Name  | Type  | Description |
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




