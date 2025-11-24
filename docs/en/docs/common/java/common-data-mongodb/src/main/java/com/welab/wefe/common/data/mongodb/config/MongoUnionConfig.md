# Basic Information

|      |      |
|------|------|
| Name | MongoUnionConfig |
| Language | .java |
| Code Path | WeFe/common/java/common-data-mongodb/src/main/java/com/welab/wefe/common/data/mongodb/config/MongoUnionConfig.java |
| Package Name | com.welab.wefe.common.data.mongodb.config |
| Dependencies | ['com.mongodb.MongoClient', 'com.mongodb.MongoClientURI', 'com.mongodb.client.MongoDatabase', 'com.mongodb.client.gridfs.GridFSBucket', 'com.mongodb.client.gridfs.GridFSBuckets', 'org.springframework.beans.factory.annotation.Value', 'org.springframework.context.annotation.Bean', 'org.springframework.context.annotation.Configuration', 'org.springframework.data.mongodb.MongoDbFactory', 'org.springframework.data.mongodb.MongoTransactionManager', 'org.springframework.data.mongodb.core.MongoTemplate', 'org.springframework.data.mongodb.core.SimpleMongoDbFactory', 'org.springframework.data.mongodb.gridfs.GridFsTemplate'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| MongoUnionConfig | class |  |



## Class MongoUnionConfig

|      |      |
|------|------|
| Access Modifier | @Configuration;public |
| Type | class |
| Name | MongoUnionConfig |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| unionUri | String |  |
| unionDatabaseName | String |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| mongoDbUnionFactory | MongoDbFactory |  |
| transactionUnionManager | MongoTransactionManager |  |
| mongoUnionClient | MongoClient |  |
| mongoUnionTemplate | MongoTemplate |  |
| gridFsTemplate | GridFsTemplate |  |
| getGridFSBucket | GridFSBucket |  |




