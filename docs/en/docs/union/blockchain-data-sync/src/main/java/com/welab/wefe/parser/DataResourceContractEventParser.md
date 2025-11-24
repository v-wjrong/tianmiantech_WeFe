# Basic Information

|      |      |
|------|------|
| Name | DataResourceContractEventParser |
| Language | .java |
| Code Path | WeFe/union/blockchain-data-sync/src/main/java/com/welab/wefe/parser/DataResourceContractEventParser.java |
| Package Name | com.welab.wefe.parser |
| Dependencies | ['com.alibaba.fastjson.JSONObject', 'com.welab.wefe.BlockchainDataSyncApp', 'com.welab.wefe.common.data.mongodb.entity.union.DataResource', 'com.welab.wefe.common.data.mongodb.entity.union.ext.DataResourceExtJSON', 'com.welab.wefe.common.data.mongodb.repo.DataResourceMongoReop', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.wefe.enums.DataResourceType', 'com.welab.wefe.constant.EventConstant', 'com.welab.wefe.exception.BusinessException', 'org.apache.commons.lang3.StringUtils'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| DataResourceContractEventParser | class |  |



## Class DataResourceContractEventParser

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | DataResourceContractEventParser |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| dataResourceMongoReop = BlockchainDataSyncApp.CONTEXT.getBean(DataResourceMongoReop.class) | DataResourceMongoReop |  |
| extJSON | DataResourceExtJSON |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| parseContractEvent | void |  |
| parseDeleteByDataResourceId | void |  |
| parseInsertEvent | void |  |
| parseUpdateExtJson | void |  |
| parseUpdateEvent | void |  |
| parseUpdateEnable | void |  |
| getImageDataSet | DataResource |  |




