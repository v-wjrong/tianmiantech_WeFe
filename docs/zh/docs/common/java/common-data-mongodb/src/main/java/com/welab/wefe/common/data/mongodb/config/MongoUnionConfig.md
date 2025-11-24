# 基础信息

|      |      |
|------|------|
| 名称 | MongoUnionConfig |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-data-mongodb/src/main/java/com/welab/wefe/common/data/mongodb/config/MongoUnionConfig.java |
| 包名 | com.welab.wefe.common.data.mongodb.config |
| 依赖项 | ['com.mongodb.MongoClient', 'com.mongodb.MongoClientURI', 'com.mongodb.client.MongoDatabase', 'com.mongodb.client.gridfs.GridFSBucket', 'com.mongodb.client.gridfs.GridFSBuckets', 'org.springframework.beans.factory.annotation.Value', 'org.springframework.context.annotation.Bean', 'org.springframework.context.annotation.Configuration', 'org.springframework.data.mongodb.MongoDbFactory', 'org.springframework.data.mongodb.MongoTransactionManager', 'org.springframework.data.mongodb.core.MongoTemplate', 'org.springframework.data.mongodb.core.SimpleMongoDbFactory', 'org.springframework.data.mongodb.gridfs.GridFsTemplate'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| MongoUnionConfig | class |  |



## 类 MongoUnionConfig

|      |      |
|------|------|
| 访问范围 | @Configuration;public |
| 类型 | class |
| 名称 | MongoUnionConfig |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| unionUri | String |  |
| unionDatabaseName | String |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| mongoDbUnionFactory | MongoDbFactory |  |
| transactionUnionManager | MongoTransactionManager |  |
| mongoUnionClient | MongoClient |  |
| mongoUnionTemplate | MongoTemplate |  |
| gridFsTemplate | GridFsTemplate |  |
| getGridFSBucket | GridFSBucket |  |




