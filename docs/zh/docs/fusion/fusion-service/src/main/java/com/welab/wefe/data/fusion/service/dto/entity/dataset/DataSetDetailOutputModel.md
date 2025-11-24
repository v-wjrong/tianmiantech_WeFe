# 基础信息

|      |      |
|------|------|
| 名称 | DataSetDetailOutputModel |
| 编码语言 | .java |
| 代码路径 | WeFe/fusion/fusion-service/src/main/java/com/welab/wefe/data/fusion/service/dto/entity/dataset/DataSetDetailOutputModel.java |
| 包名 | com.welab.wefe.data.fusion.service.dto.entity.dataset |
| 依赖项 | ['com.welab.wefe.data.fusion.service.database.entity.DataSetColumnOutputModel', 'com.welab.wefe.data.fusion.service.dto.entity.AbstractOutputModel', 'com.welab.wefe.data.fusion.service.enums.DataResourceSource', 'com.welab.wefe.data.fusion.service.enums.DataResourceType', 'com.welab.wefe.data.fusion.service.enums.Progress', 'javax.persistence.EnumType', 'javax.persistence.Enumerated', 'java.util.ArrayList', 'java.util.List', 'java.util.Map'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| DataSetDetailOutputModel | class |  |



## 类 DataSetDetailOutputModel

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | DataSetDetailOutputModel |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| name | String |  |
| process | Progress |  |
| usedCount | int |  |
| description | String |  |
| processCount | Integer |  |
| dataResourceSource | DataResourceSource |  |
| statement | String |  |
| rows | String |  |
| isStoraged = false | boolean |  |
| rowCount | int |  |
| previewData | DataSetPreviewOutputModel |  |
| sourcePath | String |  |
| dataSourceId | String |  |
| type = DataResourceType.DataSet | DataResourceType |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getDataSourceId | String |  |
| setStatement | void |  |
| setDataResourceSource | void |  |
| setStoraged | void |  |
| setDescription | void |  |
| getName | String |  |
| getRowCount | int |  |
| getUsedCount | int |  |
| getDescription | String |  |
| setRows | void |  |
| setUsedCount | void |  |
| getDataResourceSource | DataResourceSource |  |
| getStatement | String |  |
| isStoraged | boolean |  |
| setRowCount | void |  |
| getType | DataResourceType |  |
| getRows | String |  |
| getSourcePath | String |  |
| setName | void |  |
| setDataSourceId | void |  |
| setSourcePath | void |  |
| setType | void |  |
| getProcessCount | Integer |  |
| setProcessCount | void |  |
| getProcess | Progress |  |
| setProcess | void |  |
| getPreviewData | DataSetPreviewOutputModel |  |
| setPreviewData | void |  |




