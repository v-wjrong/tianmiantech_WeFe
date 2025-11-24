# Basic Information

|      |      |
|------|------|
| Name | MemberServiceContractEventParser |
| Language | .java |
| Code Path | WeFe/union/blockchain-data-sync/src/main/java/com/welab/wefe/parser/MemberServiceContractEventParser.java |
| Package Name | com.welab.wefe.parser |
| Dependencies | ['com.alibaba.fastjson.JSONObject', 'com.welab.wefe.BlockchainDataSyncApp', 'com.welab.wefe.common.data.mongodb.entity.union.MemberService', 'com.welab.wefe.common.data.mongodb.entity.union.ext.MemberServiceExtJSON', 'com.welab.wefe.common.data.mongodb.repo.MemberServiceMongoReop', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.constant.EventConstant', 'com.welab.wefe.exception.BusinessException', 'org.apache.commons.lang3.StringUtils'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| MemberServiceContractEventParser | class |  |



## Class MemberServiceContractEventParser

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | MemberServiceContractEventParser |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| extJSON | MemberServiceExtJSON |  |
| memberServiceMongoReop = BlockchainDataSyncApp.CONTEXT.getBean(MemberServiceMongoReop.class) | MemberServiceMongoReop |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| parseInsertEvent | void |  |
| parseContractEvent | void |  |
| parseUpdateEvent | void |  |
| parseDeleteByServiceIdEvent | void |  |
| parseUpdateExtJson | void |  |




