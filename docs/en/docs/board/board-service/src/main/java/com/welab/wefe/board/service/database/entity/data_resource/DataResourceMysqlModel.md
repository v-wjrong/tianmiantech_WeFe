# Basic Information

|      |      |
|------|------|
| Name | DataResourceMysqlModel |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/database/entity/data_resource/DataResourceMysqlModel.java |
| Package Name | com.welab.wefe.board.service.database.entity.data_resource |
| Dependencies | ['com.alibaba.fastjson.JSONObject', 'com.alibaba.fastjson.annotation.JSONField', 'com.vladmihalcea.hibernate.type.json.JsonStringType', 'com.welab.wefe.board.service.database.entity.base.AbstractBaseMySqlModel', 'com.welab.wefe.common.wefe.enums.ComponentType', 'com.welab.wefe.common.wefe.enums.DataResourcePublicLevel', 'com.welab.wefe.common.wefe.enums.DataResourceStorageServiceType', 'com.welab.wefe.common.wefe.enums.DataResourceType', 'org.hibernate.annotations.Type', 'org.hibernate.annotations.TypeDef', 'javax.persistence', 'java.io.File', 'java.nio.file.Path', 'java.nio.file.Paths'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| DataResourceMysqlModel | class |  |



## Class DataResourceMysqlModel

|      |      |
|------|------|
| Access Modifier | @Entity(name = "data_resource");@Table(name = "data_resource");@Inheritance(strategy = InheritanceType.JOINED);@TypeDef(name = "json", typeClass = JsonStringType.class);public |
| Type | class |
| Name | DataResourceMysqlModel |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| statisticalInformation | JSONObject |  |
| description | String |  |
| dataResourceType | DataResourceType |  |
| storageResourceName | String |  |
| derivedFromTaskId | String |  |
| derivedResource | boolean |  |
| usageCountInMember | int |  |
| publicMemberList | String |  |
| storageNamespace | String |  |
| publicLevel | DataResourcePublicLevel |  |
| storageType | DataResourceStorageServiceType |  |
| usageCountInJob | int |  |
| derivedFromJobId | String |  |
| usageCountInProject | int |  |
| name | String |  |
| totalDataCount | long |  |
| tags | String |  |
| derivedFromFlowId | String |  |
| derivedFrom | ComponentType |  |
| usageCountInFlow | int |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| setDataResourceType | void |  |
| setTotalDataCount | void |  |
| setDescription | void |  |
| getDerivedFromFlowId | String |  |
| setDerivedFromFlowId | void |  |
| getDerivedFromJobId | String |  |
| setDerivedFromJobId | void |  |
| getDerivedFromTaskId | String |  |
| setDerivedFromTaskId | void |  |
| getStatisticalInformation | JSONObject |  |
| setStatisticalInformation | void |  |
| getStorageType | DataResourceStorageServiceType |  |
| getStorageResourceName | String |  |
| isDerivedResource | boolean |  |
| getDataResourceType | DataResourceType |  |
| setPublicLevel | void |  |
| getTotalDataCount | Long |  |
| getUsageCountInFlow | int |  |
| setStorageNamespace | void |  |
| getTags | String |  |
| setUsageCountInMember | void |  |
| setUsageCountInJob | void |  |
| dir | Path |  |
| setDerivedFrom | void |  |
| setTags | void |  |
| setName | void |  |
| getUsageCountInProject | int |  |
| getPublicMemberList | String |  |
| file | File |  |
| getPublicLevel | DataResourcePublicLevel |  |
| getStorageNamespace | String |  |
| getUsageCountInMember | int |  |
| getUsageCountInJob | int |  |
| setUsageCountInFlow | void |  |
| getName | String |  |
| getDerivedFrom | ComponentType |  |
| getDescription | String |  |
| setPublicMemberList | void |  |
| setStorageType | void |  |
| setUsageCountInProject | void |  |
| setDerivedResource | void |  |
| setStorageResourceName | void |  |




