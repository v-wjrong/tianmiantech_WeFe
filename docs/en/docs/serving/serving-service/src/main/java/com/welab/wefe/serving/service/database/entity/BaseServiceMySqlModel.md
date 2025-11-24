# Basic Information

|      |      |
|------|------|
| Name | BaseServiceMySqlModel |
| Language | .java |
| Code Path | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/database/entity/BaseServiceMySqlModel.java |
| Package Name | com.welab.wefe.serving.service.database.entity |
| Dependencies | ['javax.persistence.Column', 'javax.persistence.Entity', 'javax.persistence.Inheritance', 'javax.persistence.InheritanceType', 'javax.persistence.Table', 'org.hibernate.annotations.TypeDef', 'com.vladmihalcea.hibernate.type.json.JsonStringType'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| BaseServiceMySqlModel | class |  |



## Class BaseServiceMySqlModel

|      |      |
|------|------|
| Access Modifier | @Entity(name = "base_service");@Table(name = "base_service");@Inheritance(strategy = InheritanceType.JOINED);@TypeDef(name = "json", typeClass = JsonStringType.class);public |
| Type | class |
| Name | BaseServiceMySqlModel |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| url | String |  |
| status = 0 | int |  |
| name | String |  |
| serviceType | int |  |
| serialVersionUID = 6086376958829410311L | long |  |
| serviceId = super.getId() | String |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getServiceId | String |  |
| setUrl | void |  |
| getName | String |  |
| setServiceType | void |  |
| getServiceType | int |  |
| getUrl | String |  |
| setServiceId | void |  |
| setName | void |  |
| getStatus | int |  |
| setStatus | void |  |
| isModelService | boolean |  |




