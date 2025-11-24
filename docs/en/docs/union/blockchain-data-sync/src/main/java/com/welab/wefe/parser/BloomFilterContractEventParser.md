# Basic Information

|      |      |
|------|------|
| Name | BloomFilterContractEventParser |
| Language | .java |
| Code Path | WeFe/union/blockchain-data-sync/src/main/java/com/welab/wefe/parser/BloomFilterContractEventParser.java |
| Package Name | com.welab.wefe.parser |
| Dependencies | ['com.alibaba.fastjson.JSONObject', 'com.welab.wefe.BlockchainDataSyncApp', 'com.welab.wefe.common.data.mongodb.entity.union.BloomFilter', 'com.welab.wefe.common.data.mongodb.entity.union.ext.BloomFilterExtJSON', 'com.welab.wefe.common.data.mongodb.repo.BloomFilterMongoReop', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.constant.EventConstant', 'com.welab.wefe.exception.BusinessException', 'org.apache.commons.lang3.StringUtils'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| BloomFilterContractEventParser | class |  |



## Class BloomFilterContractEventParser

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | BloomFilterContractEventParser |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| bloomFilterMongoReop = BlockchainDataSyncApp.CONTEXT.getBean(BloomFilterMongoReop.class) | BloomFilterMongoReop |  |
| extJSON | BloomFilterExtJSON |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getBloomFilter | BloomFilter |  |
| parseContractEvent | void |  |
| parseInsertEvent | void |  |
| parseUpdateHashFuntionEvent | void |  |
| parseUpdateExtJson | void |  |
| parseDeleteByDataResourceId | void |  |




