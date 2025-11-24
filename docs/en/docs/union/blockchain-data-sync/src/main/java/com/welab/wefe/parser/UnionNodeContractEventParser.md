# Basic Information

|      |      |
|------|------|
| Name | UnionNodeContractEventParser |
| Language | .java |
| Code Path | WeFe/union/blockchain-data-sync/src/main/java/com/welab/wefe/parser/UnionNodeContractEventParser.java |
| Package Name | com.welab.wefe.parser |
| Dependencies | ['com.alibaba.fastjson.JSONObject', 'com.welab.wefe.BlockchainDataSyncApp', 'com.welab.wefe.common.data.mongodb.entity.union.UnionNode', 'com.welab.wefe.common.data.mongodb.entity.union.ext.UnionNodeExtJSON', 'com.welab.wefe.common.data.mongodb.repo.UnionNodeMongoRepo', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.constant.EventConstant', 'com.welab.wefe.exception.BusinessException', 'org.apache.commons.lang3.StringUtils'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| UnionNodeContractEventParser | class |  |



## Class UnionNodeContractEventParser

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | UnionNodeContractEventParser |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| extJSON | UnionNodeExtJSON |  |
| unionNodeMongoRepo = BlockchainDataSyncApp.CONTEXT.getBean(UnionNodeMongoRepo.class) | UnionNodeMongoRepo |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| parseUpdateExtJson | void |  |
| parseDeleteByUnionNodeIdEvent | void |  |
| parseInsertEvent | void |  |
| parseContractEvent | void |  |
| parseUpdateEnableEvent | void |  |
| parseUpdatePublicKeyEvent | void |  |
| parseUpdateEvent | void |  |




