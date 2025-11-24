# 基础信息

|      |      |
|------|------|
| 名称 | DataSetDefaultTag |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-data-mongodb/src/main/java/com/welab/wefe/common/data/mongodb/entity/union/DataSetDefaultTag.java |
| 包名 | com.welab.wefe.common.data.mongodb.entity.union |
| 依赖项 | ['com.welab.wefe.common.data.mongodb.constant.MongodbTable', 'com.welab.wefe.common.data.mongodb.entity.base.AbstractBlockChainBusinessModel', 'com.welab.wefe.common.data.mongodb.entity.union.ext.DataSetDefaultTagExtJSON', 'org.springframework.data.mongodb.core.mapping.Document', 'java.util.UUID'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| DataSetDefaultTag | class |  |



## 类 DataSetDefaultTag

|      |      |
|------|------|
| 访问范围 | @Document(collection = MongodbTable.Union.DATA_SET_DEFAULT_TAG);public |
| 类型 | class |
| 名称 | DataSetDefaultTag |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| tagName | String |  |
| extJson = new DataSetDefaultTagExtJSON() | DataSetDefaultTagExtJSON |  |
| tagId = UUID.randomUUID().toString().replaceAll("-", "") | String |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getExtJson | DataSetDefaultTagExtJSON |  |
| setTagId | void |  |
| setExtJson | void |  |
| getTagName | String |  |
| setTagName | void |  |
| getTagId | String |  |




