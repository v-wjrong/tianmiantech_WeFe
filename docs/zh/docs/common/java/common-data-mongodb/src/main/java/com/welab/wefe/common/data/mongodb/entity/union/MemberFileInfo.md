# 基础信息

|      |      |
|------|------|
| 名称 | MemberFileInfo |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-data-mongodb/src/main/java/com/welab/wefe/common/data/mongodb/entity/union/MemberFileInfo.java |
| 包名 | com.welab.wefe.common.data.mongodb.entity.union |
| 依赖项 | ['com.welab.wefe.common.data.mongodb.constant.MongodbTable', 'com.welab.wefe.common.data.mongodb.entity.base.AbstractBlockChainBusinessModel', 'com.welab.wefe.common.data.mongodb.entity.union.ext.MemberFileInfoExtJSON', 'org.springframework.data.mongodb.core.mapping.Document'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| MemberFileInfo | class |  |



## 类 MemberFileInfo

|      |      |
|------|------|
| 访问范围 | @Document(collection = MongodbTable.Union.MEMBER_FILE_INFO);public |
| 类型 | class |
| 名称 | MemberFileInfo |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
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

### 方法列表

| 名称  | 类型  | 说明 |
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




