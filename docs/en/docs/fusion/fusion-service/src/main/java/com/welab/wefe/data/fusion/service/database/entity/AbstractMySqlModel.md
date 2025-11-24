# Basic Information

|      |      |
|------|------|
| Name | AbstractMySqlModel |
| Language | .java |
| Code Path | WeFe/fusion/fusion-service/src/main/java/com/welab/wefe/data/fusion/service/database/entity/AbstractMySqlModel.java |
| Package Name | com.welab.wefe.data.fusion.service.database.entity |
| Dependencies | ['javax.persistence.Column', 'javax.persistence.Id', 'javax.persistence.MappedSuperclass', 'java.io.Serializable', 'java.util.Date', 'java.util.UUID'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| AbstractMySqlModel | class |  |



## Class AbstractMySqlModel

|      |      |
|------|------|
| Access Modifier | @MappedSuperclass;public abstract |
| Type | class |
| Name | AbstractMySqlModel |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| updatedTime | Date |  |
| id = UUID.randomUUID().toString().replaceAll("-", "") | String |  |
| createdTime = new Date() | Date |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getUpdatedTime | Date |  |
| getCreatedTime | Date |  |
| getId | String |  |
| setCreatedTime | void |  |
| setId | void |  |
| setUpdatedTime | void |  |




