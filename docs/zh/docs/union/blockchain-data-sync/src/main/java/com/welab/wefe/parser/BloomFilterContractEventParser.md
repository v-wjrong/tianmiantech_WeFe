# 基础信息

|      |      |
|------|------|
| 名称 | BloomFilterContractEventParser |
| 编码语言 | .java |
| 代码路径 | WeFe/union/blockchain-data-sync/src/main/java/com/welab/wefe/parser/BloomFilterContractEventParser.java |
| 包名 | com.welab.wefe.parser |
| 依赖项 | ['com.alibaba.fastjson.JSONObject', 'com.welab.wefe.BlockchainDataSyncApp', 'com.welab.wefe.common.data.mongodb.entity.union.BloomFilter', 'com.welab.wefe.common.data.mongodb.entity.union.ext.BloomFilterExtJSON', 'com.welab.wefe.common.data.mongodb.repo.BloomFilterMongoReop', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.constant.EventConstant', 'com.welab.wefe.exception.BusinessException', 'org.apache.commons.lang3.StringUtils'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| BloomFilterContractEventParser | class |  |



## 类 BloomFilterContractEventParser

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | BloomFilterContractEventParser |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| bloomFilterMongoReop = BlockchainDataSyncApp.CONTEXT.getBean(BloomFilterMongoReop.class) | BloomFilterMongoReop |  |
| extJSON | BloomFilterExtJSON |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getBloomFilter | BloomFilter |  |
| parseContractEvent | void |  |
| parseInsertEvent | void |  |
| parseUpdateHashFuntionEvent | void |  |
| parseUpdateExtJson | void |  |
| parseDeleteByDataResourceId | void |  |




