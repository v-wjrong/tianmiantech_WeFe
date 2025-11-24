# Basic Information

|      |      |
|------|------|
| Name | MemberService |
| Language | .java |
| Code Path | WeFe/common/java/common-data-mongodb/src/main/java/com/welab/wefe/common/data/mongodb/entity/union/MemberService.java |
| Package Name | com.welab.wefe.common.data.mongodb.entity.union |
| Dependencies | ['com.welab.wefe.common.data.mongodb.constant.MongodbTable', 'com.welab.wefe.common.data.mongodb.entity.base.AbstractBlockChainBusinessModel', 'com.welab.wefe.common.data.mongodb.entity.union.ext.MemberServiceExtJSON', 'org.springframework.data.mongodb.core.mapping.Document'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| MemberService | class |  |



## Class MemberService

|      |      |
|------|------|
| Access Modifier | @Document(collection = MongodbTable.Union.MEMBER_SERVICE);public |
| Type | class |
| Name | MemberService |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| name | String |  |
| serviceId | String |  |
| memberId | String |  |
| apiName | String |  |
| serviceType | String |  |
| extJson = new MemberServiceExtJSON() | MemberServiceExtJSON |  |
| baseUrl | String |  |
| queryParams | String |  |
| serviceStatus | String |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| setBaseUrl | void |  |
| getBaseUrl | String |  |
| setApiName | void |  |
| setMemberId | void |  |
| getServiceId | String |  |
| getServiceType | String |  |
| getName | String |  |
| getExtJson | MemberServiceExtJSON |  |
| setServiceId | void |  |
| setExtJson | void |  |
| getApiName | String |  |
| setName | void |  |
| setServiceStatus | void |  |
| getMemberId | String |  |
| getServiceStatus | String |  |
| getQueryParams | String |  |
| setServiceType | void |  |
| setQueryParams | void |  |




