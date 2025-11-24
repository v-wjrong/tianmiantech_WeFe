# Basic Information

|      |      |
|------|------|
| Name | MemberContractEventParser |
| Language | .java |
| Code Path | WeFe/union/blockchain-data-sync/src/main/java/com/welab/wefe/parser/MemberContractEventParser.java |
| Package Name | com.welab.wefe.parser |
| Dependencies | ['com.alibaba.fastjson.JSONObject', 'com.welab.wefe.BlockchainDataSyncApp', 'com.welab.wefe.common.data.mongodb.entity.union.Member', 'com.welab.wefe.common.data.mongodb.entity.union.ext.MemberExtJSON', 'com.welab.wefe.common.data.mongodb.repo.MemberMongoReop', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.constant.EventConstant', 'com.welab.wefe.exception.BusinessException', 'org.apache.commons.lang3.StringUtils'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| MemberContractEventParser | class |  |



## Class MemberContractEventParser

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | MemberContractEventParser |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| memberMongoReop = BlockchainDataSyncApp.CONTEXT.getBean(MemberMongoReop.class) | MemberMongoReop |  |
| extJSON | MemberExtJSON |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| parseUpdateExcludePublicKeyEvent | void |  |
| parseInsertAndUpdateEvent | void |  |
| parseUpdateExcludeLogoEvent | void |  |
| parseUpdateLogoByIdEvent | void |  |
| parseUpdatePublicKeyEvent | void |  |
| parseContractEvent | void |  |
| parseDeleteByIdEvent | void |  |
| parserUpdateLastActivityTimeByIdEvent | void |  |
| parseUpdateExtJson | void |  |




