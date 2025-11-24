# Basic Information

|      |      |
|------|------|
| Name | ModelMemberMySqlModel |
| Language | .java |
| Code Path | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/database/entity/ModelMemberMySqlModel.java |
| Package Name | com.welab.wefe.serving.service.database.entity |
| Dependencies | ['com.welab.wefe.common.wefe.enums.JobMemberRole', 'com.welab.wefe.serving.service.enums.MemberModelStatusEnum', 'javax.persistence.Column', 'javax.persistence.Entity', 'javax.persistence.EnumType', 'javax.persistence.Enumerated'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| ModelMemberMySqlModel | class |  |



## Class ModelMemberMySqlModel

|      |      |
|------|------|
| Access Modifier | @Entity(name = "model_member");public |
| Type | class |
| Name | ModelMemberMySqlModel |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| status = MemberModelStatusEnum.offline | MemberModelStatusEnum |  |
| memberId | String |  |
| modelId | String |  |
| role | JobMemberRole |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getModelId | String |  |
| setMemberId | void |  |
| setModelId | void |  |
| getMemberId | String |  |
| getRole | JobMemberRole |  |
| setRole | void |  |
| getStatus | MemberModelStatusEnum |  |
| setStatus | void |  |




