# Basic Information

|      |      |
|------|------|
| Name | TransactionResponseService |
| Language | .java |
| Code Path | WeFe/union/blockchain-data-sync/src/main/java/com/welab/wefe/service/TransactionResponseService.java |
| Package Name | com.welab.wefe.service |
| Dependencies | ['com.welab.wefe.bo.data.BlockInfoBO', 'com.welab.wefe.bo.data.TransactionResponseBO', 'com.welab.wefe.common.data.mongodb.entity.union.TransactionResponseDetailInfo', 'com.welab.wefe.common.data.mongodb.util.QueryBuilder', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.util.StringUtil', 'org.apache.commons.collections4.CollectionUtils', 'org.fisco.bcos.sdk.transaction.model.dto.TransactionResponse', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.data.domain.Sort', 'org.springframework.data.mongodb.core.MongoTemplate', 'org.springframework.data.mongodb.core.index.Index', 'org.springframework.data.mongodb.core.query.Query', 'org.springframework.stereotype.Service', 'java.util.List', 'java.util.Set'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| TransactionResponseService | class |  |



## Class TransactionResponseService

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | TransactionResponseService |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| EMPTY_EVENT_NAME = "empty" | String |  |
| EMPTY_CONTRACT_NAME = "empty" | String |  |
| mongoTemplate | MongoTemplate |  |
| COLLECTION_NAME_PREFIX = "BlockTr_" | String |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| transactionResponseToJson | JObject |  |
| buildCollectionName | String |  |
| getByTransactionHash | TransactionResponseDetailInfo |  |
| getEventName | String |  |
| save | void |  |




