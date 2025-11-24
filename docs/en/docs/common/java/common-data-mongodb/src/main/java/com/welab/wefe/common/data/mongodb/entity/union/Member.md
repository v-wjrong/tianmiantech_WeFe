# Basic Information

|      |      |
|------|------|
| Name | Member |
| Language | .java |
| Code Path | WeFe/common/java/common-data-mongodb/src/main/java/com/welab/wefe/common/data/mongodb/entity/union/Member.java |
| Package Name | com.welab.wefe.common.data.mongodb.entity.union |
| Dependencies | ['com.welab.wefe.common.data.mongodb.constant.MongodbTable', 'com.welab.wefe.common.data.mongodb.entity.base.AbstractBlockChainBusinessModel', 'com.welab.wefe.common.data.mongodb.entity.union.ext.MemberExtJSON', 'org.springframework.data.mongodb.core.mapping.Document'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| Member | class |  |



## Class Member

|      |      |
|------|------|
| Access Modifier | @Document(collection = MongodbTable.Union.MEMBER);public |
| Type | class |
| Name | Member |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| extJson = new MemberExtJSON() | MemberExtJSON |  |
| lastActivityTime | String |  |
| gatewayUri | String |  |
| name | String |  |
| mobile | String |  |
| freezed | String |  |
| hidden | String |  |
| email | String |  |
| lostContact | String |  |
| memberId | String |  |
| logo | String |  |
| publicKey | String |  |
| allowOpenDataSet | String |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getMemberId | String |  |
| setLogo | void |  |
| setEmail | void |  |
| getEmail | String |  |
| setPublicKey | void |  |
| getLostContact | String |  |
| getHidden | String |  |
| setGatewayUri | void |  |
| setLostContact | void |  |
| setName | void |  |
| getName | String |  |
| setHidden | void |  |
| getPublicKey | String |  |
| setFreezed | void |  |
| getGatewayUri | String |  |
| setAllowOpenDataSet | void |  |
| getFreezed | String |  |
| getLogo | String |  |
| setMobile | void |  |
| getAllowOpenDataSet | String |  |
| setMemberId | void |  |
| getMobile | String |  |
| getLastActivityTime | String |  |
| setLastActivityTime | void |  |
| getExtJson | MemberExtJSON |  |
| setExtJson | void |  |




