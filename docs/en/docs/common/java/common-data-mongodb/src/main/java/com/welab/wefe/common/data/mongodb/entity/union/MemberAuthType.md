# Basic Information

|      |      |
|------|------|
| Name | MemberAuthType |
| Language | .java |
| Code Path | WeFe/common/java/common-data-mongodb/src/main/java/com/welab/wefe/common/data/mongodb/entity/union/MemberAuthType.java |
| Package Name | com.welab.wefe.common.data.mongodb.entity.union |
| Dependencies | ['com.welab.wefe.common.data.mongodb.constant.MongodbTable', 'com.welab.wefe.common.data.mongodb.entity.base.AbstractBlockChainBusinessModel', 'com.welab.wefe.common.data.mongodb.entity.union.ext.MemberAuthTypeExtJSON', 'org.springframework.data.mongodb.core.mapping.Document', 'java.util.UUID'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| MemberAuthType | class |  |



## Class MemberAuthType

|      |      |
|------|------|
| Access Modifier | @Document(collection = MongodbTable.Union.MEMBER_AUTH_TYPE);public |
| Type | class |
| Name | MemberAuthType |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| typeId = UUID.randomUUID().toString().replaceAll("-", "") | String |  |
| extJson = new MemberAuthTypeExtJSON() | MemberAuthTypeExtJSON |  |
| typeName | String |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getExtJson | MemberAuthTypeExtJSON |  |
| getTypeName | String |  |
| setTypeId | void |  |
| setTypeName | void |  |
| setExtJson | void |  |
| getTypeId | String |  |




