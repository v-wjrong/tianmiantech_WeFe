# Basic Information

|      |      |
|------|------|
| Name | MemberFileInfo |
| Language | .java |
| Code Path | WeFe/common/java/common-data-mongodb/src/main/java/com/welab/wefe/common/data/mongodb/entity/union/MemberFileInfo.java |
| Package Name | com.welab.wefe.common.data.mongodb.entity.union |
| Dependencies | ['com.welab.wefe.common.data.mongodb.constant.MongodbTable', 'com.welab.wefe.common.data.mongodb.entity.base.AbstractBlockChainBusinessModel', 'com.welab.wefe.common.data.mongodb.entity.union.ext.MemberFileInfoExtJSON', 'org.springframework.data.mongodb.core.mapping.Document'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| MemberFileInfo | class |  |



## Class MemberFileInfo

|      |      |
|------|------|
| Access Modifier | @Document(collection = MongodbTable.Union.MEMBER_FILE_INFO);public |
| Type | class |
| Name | MemberFileInfo |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| describe | String |  |
| fileId | String |  |
| blockchainNodeId | String |  |
| memberId | String |  |
| fileName | String |  |
| filePublicLevel | String |  |
| rurpose | String |  |
| extJson = new MemberFileInfoExtJSON() | MemberFileInfoExtJSON |  |
| fileSize | String |  |
| fileSign | String |  |
| enable = "1" | String |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getFileName | String |  |
| setFileSign | void |  |
| setFileSize | void |  |
| getMemberId | String |  |
| setFileName | void |  |
| getDescribe | String |  |
| setBlockchainNodeId | void |  |
| getFileId | String |  |
| setMemberId | void |  |
| setDescribe | void |  |
| getRurpose | String |  |
| setRurpose | void |  |
| getFileSize | String |  |
| setFileId | void |  |
| getFileSign | String |  |
| getBlockchainNodeId | String |  |
| getEnable | String |  |
| setEnable | void |  |
| getFilePublicLevel | String |  |
| setFilePublicLevel | void |  |
| getExtJson | MemberFileInfoExtJSON |  |
| setExtJson | void |  |




