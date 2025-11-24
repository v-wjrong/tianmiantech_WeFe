# Basic Information

|      |      |
|------|------|
| Name | BloomFilter |
| Language | .java |
| Code Path | WeFe/common/java/common-data-mongodb/src/main/java/com/welab/wefe/common/data/mongodb/entity/union/BloomFilter.java |
| Package Name | com.welab.wefe.common.data.mongodb.entity.union |
| Dependencies | ['com.welab.wefe.common.data.mongodb.constant.MongodbTable', 'com.welab.wefe.common.data.mongodb.entity.base.AbstractBlockChainBusinessModel', 'com.welab.wefe.common.data.mongodb.entity.union.ext.BloomFilterExtJSON', 'com.welab.wefe.common.data.mongodb.entity.union.ext.DataResourceExtJSON', 'org.springframework.data.mongodb.core.mapping.Document'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| BloomFilter | class |  |



## Class BloomFilter

|      |      |
|------|------|
| Access Modifier | @Document(collection = MongodbTable.Union.BLOOM_FILTER);public |
| Type | class |
| Name | BloomFilter |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| dataResourceId | String |  |
| hashFunction | String |  |
| extJson = new BloomFilterExtJSON() | BloomFilterExtJSON |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getDataResourceId | String |  |
| getExtJson | BloomFilterExtJSON |  |
| setExtJson | void |  |
| getHashFunction | String |  |
| setDataResourceId | void |  |
| setHashFunction | void |  |




