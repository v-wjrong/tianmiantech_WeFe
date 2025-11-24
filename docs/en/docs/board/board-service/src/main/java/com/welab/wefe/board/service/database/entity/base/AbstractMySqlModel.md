# Basic Information

|      |      |
|------|------|
| Name | AbstractMySqlModel |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/database/entity/base/AbstractMySqlModel.java |
| Package Name | com.welab.wefe.board.service.database.entity.base |
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
| id = UUID.randomUUID().toString().replaceAll("-", "") | String |  |
| createdTime = new Date() | Date |  |
| updatedTime | Date |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getUpdatedTime | Date |  |
| getCreatedTime | Date |  |
| setCreatedTime | void |  |
| setId | void |  |
| setUpdatedTime | void |  |
| getId | String |  |




