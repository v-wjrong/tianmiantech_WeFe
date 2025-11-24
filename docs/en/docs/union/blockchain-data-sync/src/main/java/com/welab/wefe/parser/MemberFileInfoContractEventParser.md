# Basic Information

|      |      |
|------|------|
| Name | MemberFileInfoContractEventParser |
| Language | .java |
| Code Path | WeFe/union/blockchain-data-sync/src/main/java/com/welab/wefe/parser/MemberFileInfoContractEventParser.java |
| Package Name | com.welab.wefe.parser |
| Dependencies | ['com.alibaba.fastjson.JSONObject', 'com.welab.wefe.BlockchainDataSyncApp', 'com.welab.wefe.common.data.mongodb.entity.union.MemberFileInfo', 'com.welab.wefe.common.data.mongodb.entity.union.ext.MemberFileInfoExtJSON', 'com.welab.wefe.common.data.mongodb.repo.MemberFileInfoMongoRepo', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.constant.EventConstant', 'com.welab.wefe.exception.BusinessException', 'org.apache.commons.lang3.StringUtils'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| MemberFileInfoContractEventParser | class |  |



## Class MemberFileInfoContractEventParser

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | MemberFileInfoContractEventParser |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| extJSON | MemberFileInfoExtJSON |  |
| unionNodeMongoRepo = BlockchainDataSyncApp.CONTEXT.getBean(MemberFileInfoMongoRepo.class) | MemberFileInfoMongoRepo |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| parseUpdateEnableEvent | void |  |
| parseInsertEvent | void |  |
| parseContractEvent | void |  |
| parseUpdateExtJson | void |  |




