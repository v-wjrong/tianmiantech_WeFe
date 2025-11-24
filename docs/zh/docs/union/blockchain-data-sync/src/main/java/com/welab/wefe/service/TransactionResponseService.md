# 基础信息

|      |      |
|------|------|
| 名称 | TransactionResponseService |
| 编码语言 | .java |
| 代码路径 | WeFe/union/blockchain-data-sync/src/main/java/com/welab/wefe/service/TransactionResponseService.java |
| 包名 | com.welab.wefe.service |
| 依赖项 | ['com.welab.wefe.bo.data.BlockInfoBO', 'com.welab.wefe.bo.data.TransactionResponseBO', 'com.welab.wefe.common.data.mongodb.entity.union.TransactionResponseDetailInfo', 'com.welab.wefe.common.data.mongodb.util.QueryBuilder', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.util.StringUtil', 'org.apache.commons.collections4.CollectionUtils', 'org.fisco.bcos.sdk.transaction.model.dto.TransactionResponse', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.data.domain.Sort', 'org.springframework.data.mongodb.core.MongoTemplate', 'org.springframework.data.mongodb.core.index.Index', 'org.springframework.data.mongodb.core.query.Query', 'org.springframework.stereotype.Service', 'java.util.List', 'java.util.Set'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| TransactionResponseService | class |  |



## 类 TransactionResponseService

|      |      |
|------|------|
| 访问范围 | @Service;public |
| 类型 | class |
| 名称 | TransactionResponseService |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| EMPTY_EVENT_NAME = "empty" | String |  |
| EMPTY_CONTRACT_NAME = "empty" | String |  |
| mongoTemplate | MongoTemplate |  |
| COLLECTION_NAME_PREFIX = "BlockTr_" | String |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| transactionResponseToJson | JObject |  |
| buildCollectionName | String |  |
| getByTransactionHash | TransactionResponseDetailInfo |  |
| getEventName | String |  |
| save | void |  |




