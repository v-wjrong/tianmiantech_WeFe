# 基础信息

|      |      |
|------|------|
| 名称 | DataSet |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-data-mongodb/src/main/java/com/welab/wefe/common/data/mongodb/entity/union/DataSet.java |
| 包名 | com.welab.wefe.common.data.mongodb.entity.union |
| 依赖项 | ['com.welab.wefe.common.data.mongodb.constant.MongodbTable', 'com.welab.wefe.common.data.mongodb.entity.base.AbstractBlockChainBusinessModel', 'com.welab.wefe.common.data.mongodb.entity.union.ext.DataSetExtJSON', 'org.springframework.data.mongodb.core.mapping.Document'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| DataSet | class |  |



## 类 DataSet

|      |      |
|------|------|
| 访问范围 | @Document(collection = MongodbTable.Union.DATASET);public |
| 类型 | class |
| 名称 | DataSet |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| description | String |  |
| memberId | String |  |
| featureCount | String |  |
| columnNameList | String |  |
| usageCountInFlow | String |  |
| featureNameList | String |  |
| dataSetId | String |  |
| usageCountInProject | String |  |
| rowCount | String |  |
| usageCountInJob | String |  |
| containsY | String |  |
| publicLevel | String |  |
| tags | String |  |
| name | String |  |
| columnCount | String |  |
| publicMemberList | String |  |
| extJson = new DataSetExtJSON() | DataSetExtJSON |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| setColumnCount | void |  |
| getDataSetId | String |  |
| getUsageCountInFlow | String |  |
| getFeatureCount | String |  |
| getRowCount | String |  |
| setPublicMemberList | void |  |
| getUsageCountInJob | String |  |
| getPublicLevel | String |  |
| setFeatureNameList | void |  |
| getContainsY | String |  |
| setRowCount | void |  |
| getMemberId | String |  |
| setMemberId | void |  |
| getColumnNameList | String |  |
| setUsageCountInFlow | void |  |
| setColumnNameList | void |  |
| setName | void |  |
| setDataSetId | void |  |
| getPublicMemberList | String |  |
| getColumnCount | String |  |
| getUsageCountInProject | String |  |
| setPublicLevel | void |  |
| setUsageCountInJob | void |  |
| setTags | void |  |
| getExtJson | DataSetExtJSON |  |
| setContainsY | void |  |
| setFeatureCount | void |  |
| getFeatureNameList | String |  |
| getName | String |  |
| setUsageCountInProject | void |  |
| getDescription | String |  |
| setDescription | void |  |
| getTags | String |  |
| setExtJson | void |  |




