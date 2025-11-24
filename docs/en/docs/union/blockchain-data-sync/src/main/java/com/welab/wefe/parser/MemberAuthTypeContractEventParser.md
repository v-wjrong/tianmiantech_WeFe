# Basic Information

|      |      |
|------|------|
| Name | MemberAuthTypeContractEventParser |
| Language | .java |
| Code Path | WeFe/union/blockchain-data-sync/src/main/java/com/welab/wefe/parser/MemberAuthTypeContractEventParser.java |
| Package Name | com.welab.wefe.parser |
| Dependencies | ['com.alibaba.fastjson.JSONObject', 'com.welab.wefe.BlockchainDataSyncApp', 'com.welab.wefe.common.data.mongodb.entity.union.MemberAuthType', 'com.welab.wefe.common.data.mongodb.entity.union.ext.MemberAuthTypeExtJSON', 'com.welab.wefe.common.data.mongodb.repo.MemberAuthTypeMongoRepo', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.constant.EventConstant', 'com.welab.wefe.exception.BusinessException', 'org.apache.commons.lang3.StringUtils'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| MemberAuthTypeContractEventParser | class |  |



## Class MemberAuthTypeContractEventParser

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | MemberAuthTypeContractEventParser |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| extJSON | MemberAuthTypeExtJSON |  |
| memberAuthTypeMongoRepo = BlockchainDataSyncApp.CONTEXT.getBean(MemberAuthTypeMongoRepo.class) | MemberAuthTypeMongoRepo |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| parseUpdateEvent | void |  |
| parseUpdateExtJson | void |  |
| parseContractEvent | void |  |
| parseInsertEvent | void |  |
| parseDeleteByTypeIdEvent | void |  |




