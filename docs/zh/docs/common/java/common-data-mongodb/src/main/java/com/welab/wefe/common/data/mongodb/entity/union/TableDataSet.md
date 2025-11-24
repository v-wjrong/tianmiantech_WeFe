# 基础信息

|      |      |
|------|------|
| 名称 | TableDataSet |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-data-mongodb/src/main/java/com/welab/wefe/common/data/mongodb/entity/union/TableDataSet.java |
| 包名 | com.welab.wefe.common.data.mongodb.entity.union |
| 依赖项 | ['com.welab.wefe.common.data.mongodb.constant.MongodbTable', 'com.welab.wefe.common.data.mongodb.entity.base.AbstractBlockChainBusinessModel', 'com.welab.wefe.common.data.mongodb.entity.union.ext.DataResourceExtJSON', 'com.welab.wefe.common.data.mongodb.entity.union.ext.TableDataSetExtJSON', 'org.springframework.data.mongodb.core.mapping.Document'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| TableDataSet | class |  |



## 类 TableDataSet

|      |      |
|------|------|
| 访问范围 | @Document(collection = MongodbTable.Union.TABLE_DATASET);public |
| 类型 | class |
| 名称 | TableDataSet |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| containsY | String |  |
| dataResourceId | String |  |
| columnCount | String |  |
| extJson = new TableDataSetExtJSON() | TableDataSetExtJSON |  |
| columnNameList | String |  |
| featureCount | String |  |
| featureNameList | String |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| setFeatureCount | void |  |
| getFeatureCount | String |  |
| setContainsY | void |  |
| getExtJson | TableDataSetExtJSON |  |
| getContainsY | String |  |
| getFeatureNameList | String |  |
| getColumnCount | String |  |
| setColumnNameList | void |  |
| setDataResourceId | void |  |
| setFeatureNameList | void |  |
| getColumnNameList | String |  |
| setColumnCount | void |  |
| getDataResourceId | String |  |
| setExtJson | void |  |




