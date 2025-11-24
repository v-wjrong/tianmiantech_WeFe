# Basic Information

|      |      |
|------|------|
| Name | AbstractUniqueIDEntity |
| Language | .java |
| Code Path | WeFe/common/java/common-data-mysql/src/main/java/com/welab/wefe/common/data/mysql/entity/AbstractUniqueIDEntity.java |
| Package Name | com.welab.wefe.common.data.mysql.entity |
| Dependencies | ['javax.persistence.Id', 'javax.persistence.MappedSuperclass', 'java.util.UUID'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| AbstractUniqueIDEntity | class |  |



## Class AbstractUniqueIDEntity

|      |      |
|------|------|
| Access Modifier | @MappedSuperclass;public |
| Type | class |
| Name | AbstractUniqueIDEntity |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| id = UUID.randomUUID().toString().replaceAll("-", "") | String |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getId | String |  |
| setId | void |  |




