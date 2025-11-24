# 基础信息

|      |      |
|------|------|
| 名称 | DataResourceLazyUpdateModel |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-data-mongodb/src/main/java/com/welab/wefe/common/data/mongodb/entity/union/DataResourceLazyUpdateModel.java |
| 包名 | com.welab.wefe.common.data.mongodb.entity.union |
| 依赖项 | ['com.welab.wefe.common.data.mongodb.constant.MongodbTable', 'com.welab.wefe.common.data.mongodb.entity.base.AbstractNormalMongoModel', 'com.welab.wefe.common.wefe.enums.DataResourceType', 'org.springframework.data.mongodb.core.mapping.Document'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| DataResourceLazyUpdateModel | class |  |



## 类 DataResourceLazyUpdateModel

|      |      |
|------|------|
| 访问范围 | @Document(collection = MongodbTable.Union.DATA_RESOURCE_LAZY_UPDATE_MODEL);public |
| 类型 | class |
| 名称 | DataResourceLazyUpdateModel |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| usageCountInMember | int |  |
| labeledCount | int |  |
| dataResourceId | String |  |
| labelCompleted | boolean |  |
| usageCountInJob | int |  |
| labelList | String |  |
| usageCountInFlow | int |  |
| totalDataCount | int |  |
| usageCountInProject | int |  |
| dataResourceType | DataResourceType |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getUsageCountInFlow | int |  |
| setUsageCountInProject | void |  |
| setUsageCountInMember | void |  |
| setTotalDataCount | void |  |
| getUsageCountInJob | int |  |
| isLabelCompleted | boolean |  |
| setUsageCountInFlow | void |  |
| getTotalDataCount | int |  |
| getLabeledCount | int |  |
| setLabelList | void |  |
| setDataResourceId | void |  |
| getLabelList | String |  |
| setLabeledCount | void |  |
| getUsageCountInProject | int |  |
| getUsageCountInMember | int |  |
| getDataResourceId | String |  |
| setUsageCountInJob | void |  |
| setLabelCompleted | void |  |
| getDataResourceType | DataResourceType |  |
| setDataResourceType | void |  |




