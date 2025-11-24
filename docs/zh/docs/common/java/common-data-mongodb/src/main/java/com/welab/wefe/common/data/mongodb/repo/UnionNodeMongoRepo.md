# 基础信息

|      |      |
|------|------|
| 名称 | UnionNodeMongoRepo |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-data-mongodb/src/main/java/com/welab/wefe/common/data/mongodb/repo/UnionNodeMongoRepo.java |
| 包名 | com.welab.wefe.common.data.mongodb.repo |
| 依赖项 | ['com.mongodb.client.result.UpdateResult', 'com.welab.wefe.common.data.mongodb.entity.union.UnionNode', 'com.welab.wefe.common.data.mongodb.entity.union.ext.UnionNodeExtJSON', 'com.welab.wefe.common.data.mongodb.util.QueryBuilder', 'com.welab.wefe.common.data.mongodb.util.UpdateBuilder', 'org.apache.commons.lang3.StringUtils', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.data.mongodb.core.MongoTemplate', 'org.springframework.data.mongodb.core.query.Query', 'org.springframework.data.mongodb.core.query.Update', 'org.springframework.stereotype.Repository', 'java.util.List'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| UnionNodeMongoRepo | class |  |



## 类 UnionNodeMongoRepo

|      |      |
|------|------|
| 访问范围 | @Repository;public |
| 类型 | class |
| 名称 | UnionNodeMongoRepo |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| mongoUnionTemplate | MongoTemplate |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| update | boolean |  |
| findAll | List<UnionNode> |  |
| getMongoTemplate | MongoTemplate |  |
| findExcludeCurrentNode | List<UnionNode> |  |
| findByBlockchainNodeId | UnionNode |  |
| deleteByUnionNodeId | boolean |  |
| findByNodeId | UnionNode |  |
| findByUnionBaseUrl | UnionNode |  |
| updateEnable | boolean |  |
| updatePublicKey | boolean |  |
| updateExtJSONById | boolean |  |




