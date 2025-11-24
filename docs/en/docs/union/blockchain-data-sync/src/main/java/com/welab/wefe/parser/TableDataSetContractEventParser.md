# Basic Information

|      |      |
|------|------|
| Name | TableDataSetContractEventParser |
| Language | .java |
| Code Path | WeFe/union/blockchain-data-sync/src/main/java/com/welab/wefe/parser/TableDataSetContractEventParser.java |
| Package Name | com.welab.wefe.parser |
| Dependencies | ['com.alibaba.fastjson.JSONObject', 'com.welab.wefe.BlockchainDataSyncApp', 'com.welab.wefe.common.data.mongodb.entity.union.TableDataSet', 'com.welab.wefe.common.data.mongodb.entity.union.ext.TableDataSetExtJSON', 'com.welab.wefe.common.data.mongodb.repo.TableDataSetMongoReop', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.constant.EventConstant', 'com.welab.wefe.exception.BusinessException', 'org.apache.commons.lang3.StringUtils'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| TableDataSetContractEventParser | class |  |



## Class TableDataSetContractEventParser

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | TableDataSetContractEventParser |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| tableDataSetMongoReop = BlockchainDataSyncApp.CONTEXT.getBean(TableDataSetMongoReop.class) | TableDataSetMongoReop |  |
| extJSON | TableDataSetExtJSON |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| parseContractEvent | void |  |
| parseInsertEvent | void |  |
| parseUpdateEvent | void |  |
| parseUpdateExtJson | void |  |
| parseDeleteByDataResourceId | void |  |
| getTableDataSet | TableDataSet |  |




