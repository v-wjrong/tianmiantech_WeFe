# 基础信息

|      |      |
|------|------|
| 名称 | DataSetMySqlModel |
| 编码语言 | .java |
| 代码路径 | WeFe/fusion/fusion-service/src/main/java/com/welab/wefe/data/fusion/service/database/entity/DataSetMySqlModel.java |
| 包名 | com.welab.wefe.data.fusion.service.database.entity |
| 依赖项 | ['com.welab.wefe.data.fusion.service.enums.DataResourceSource', 'com.welab.wefe.data.fusion.service.enums.Progress', 'javax.persistence.Entity', 'javax.persistence.EnumType', 'javax.persistence.Enumerated'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| DataSetMySqlModel | class |  |



## 类 DataSetMySqlModel

|      |      |
|------|------|
| 访问范围 | @Entity(name = "data_set");public |
| 类型 | class |
| 名称 | DataSetMySqlModel |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| sourcePath | String |  |
| dataResourceSource | DataResourceSource |  |
| rows | String |  |
| description | String |  |
| name | String |  |
| processCount = 0 | Integer |  |
| usedCount = 0 | int |  |
| statement | String |  |
| isStoraged = false | boolean |  |
| process | Progress |  |
| dataSourceId | String |  |
| rowCount = 0 | Integer |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| setRows | void |  |
| setStatement | void |  |
| setName | void |  |
| setDescription | void |  |
| getUsedCount | int |  |
| getProcess | Progress |  |
| getDataResourceSource | DataResourceSource |  |
| getDataSourceId | String |  |
| getRows | String |  |
| getName | String |  |
| setDataResourceSource | void |  |
| setProcess | void |  |
| getRowCount | Integer |  |
| isStoraged | boolean |  |
| getProcessCount | Integer |  |
| getStatement | String |  |
| setDataSourceId | void |  |
| setProcessCount | void |  |
| getSourcePath | String |  |
| setStoraged | void |  |
| getDescription | String |  |
| setSourcePath | void |  |
| setRowCount | void |  |
| setUsedCount | void |  |




