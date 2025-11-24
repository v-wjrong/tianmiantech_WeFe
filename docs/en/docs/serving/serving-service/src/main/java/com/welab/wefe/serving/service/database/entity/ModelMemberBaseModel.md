# Basic Information

|      |      |
|------|------|
| Name | ModelMemberBaseModel |
| Language | .java |
| Code Path | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/database/entity/ModelMemberBaseModel.java |
| Package Name | com.welab.wefe.serving.service.database.entity |
| Dependencies | ['javax.persistence.Column', 'javax.persistence.Entity', 'javax.persistence.Id', 'java.util.UUID'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| ModelMemberBaseModel | class |  |



## Class ModelMemberBaseModel

|      |      |
|------|------|
| Access Modifier | @Entity(name = "model_member_base");public |
| Type | class |
| Name | ModelMemberBaseModel |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| id = UUID.randomUUID().toString().replaceAll("-", "") | String |  |
| role | String |  |
| api | String |  |
| memberId | String |  |
| modelId | String |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| setMemberId | void |  |
| getId | String |  |
| getRole | String |  |
| getMemberId | String |  |
| setModelId | void |  |
| setId | void |  |
| setRole | void |  |
| getApi | String |  |
| getModelId | String |  |
| setApi | void |  |




