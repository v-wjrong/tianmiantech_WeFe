# 基础信息

|      |      |
|------|------|
| 名称 | BloomFilter |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-data-mongodb/src/main/java/com/welab/wefe/common/data/mongodb/entity/union/BloomFilter.java |
| 包名 | com.welab.wefe.common.data.mongodb.entity.union |
| 依赖项 | ['com.welab.wefe.common.data.mongodb.constant.MongodbTable', 'com.welab.wefe.common.data.mongodb.entity.base.AbstractBlockChainBusinessModel', 'com.welab.wefe.common.data.mongodb.entity.union.ext.BloomFilterExtJSON', 'com.welab.wefe.common.data.mongodb.entity.union.ext.DataResourceExtJSON', 'org.springframework.data.mongodb.core.mapping.Document'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| BloomFilter | class |  |



## 类 BloomFilter

|      |      |
|------|------|
| 访问范围 | @Document(collection = MongodbTable.Union.BLOOM_FILTER);public |
| 类型 | class |
| 名称 | BloomFilter |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| dataResourceId | String |  |
| hashFunction | String |  |
| extJson = new BloomFilterExtJSON() | BloomFilterExtJSON |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getDataResourceId | String |  |
| getExtJson | BloomFilterExtJSON |  |
| setExtJson | void |  |
| getHashFunction | String |  |
| setDataResourceId | void |  |
| setHashFunction | void |  |




