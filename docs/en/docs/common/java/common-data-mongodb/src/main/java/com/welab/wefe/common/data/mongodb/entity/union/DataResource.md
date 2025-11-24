# Basic Information

|      |      |
|------|------|
| Name | DataResource |
| Language | .java |
| Code Path | WeFe/common/java/common-data-mongodb/src/main/java/com/welab/wefe/common/data/mongodb/entity/union/DataResource.java |
| Package Name | com.welab.wefe.common.data.mongodb.entity.union |
| Dependencies | ['com.welab.wefe.common.data.mongodb.constant.MongodbTable', 'com.welab.wefe.common.data.mongodb.entity.base.AbstractBlockChainBusinessModel', 'com.welab.wefe.common.data.mongodb.entity.union.ext.DataResourceExtJSON', 'com.welab.wefe.common.wefe.enums.DataResourceType', 'org.springframework.data.mongodb.core.mapping.Document'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| DataResource | class |  |



## Class DataResource

|      |      |
|------|------|
| Access Modifier | @Document(collection = MongodbTable.Union.DATA_RESOURCE);public |
| Type | class |
| Name | DataResource |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| tags | String |  |
| dataResourceId | String |  |
| description | String |  |
| memberId | String |  |
| extJson = new DataResourceExtJSON() | DataResourceExtJSON |  |
| totalDataCount | String |  |
| usageCountInJob | String |  |
| enable | String |  |
| publicLevel | String |  |
| usageCountInFlow | String |  |
| publicMemberList | String |  |
| usageCountInProject | String |  |
| name | String |  |
| dataResourceType | DataResourceType |  |
| usageCountInMember | String |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getUsageCountInFlow | String |  |
| setExtJson | void |  |
| getMemberId | String |  |
| getUsageCountInJob | String |  |
| setUsageCountInJob | void |  |
| setDataResourceId | void |  |
| getUsageCountInMember | String |  |
| getPublicLevel | String |  |
| setUsageCountInFlow | void |  |
| setName | void |  |
| getDataResourceId | String |  |
| setUsageCountInMember | void |  |
| getTags | String |  |
| setUsageCountInProject | void |  |
| getDescription | String |  |
| setPublicLevel | void |  |
| setTotalDataCount | void |  |
| getExtJson | DataResourceExtJSON |  |
| setDataResourceType | void |  |
| setDescription | void |  |
| setEnable | void |  |
| setMemberId | void |  |
| getPublicMemberList | String |  |
| getTotalDataCount | String |  |
| getDataResourceType | DataResourceType |  |
| setTags | void |  |
| getEnable | String |  |
| getUsageCountInProject | String |  |
| setPublicMemberList | void |  |
| getName | String |  |




