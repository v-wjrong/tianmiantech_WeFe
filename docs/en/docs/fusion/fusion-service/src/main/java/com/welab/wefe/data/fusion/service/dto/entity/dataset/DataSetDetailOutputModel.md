# Basic Information

|      |      |
|------|------|
| Name | DataSetDetailOutputModel |
| Language | .java |
| Code Path | WeFe/fusion/fusion-service/src/main/java/com/welab/wefe/data/fusion/service/dto/entity/dataset/DataSetDetailOutputModel.java |
| Package Name | com.welab.wefe.data.fusion.service.dto.entity.dataset |
| Dependencies | ['com.welab.wefe.data.fusion.service.database.entity.DataSetColumnOutputModel', 'com.welab.wefe.data.fusion.service.dto.entity.AbstractOutputModel', 'com.welab.wefe.data.fusion.service.enums.DataResourceSource', 'com.welab.wefe.data.fusion.service.enums.DataResourceType', 'com.welab.wefe.data.fusion.service.enums.Progress', 'javax.persistence.EnumType', 'javax.persistence.Enumerated', 'java.util.ArrayList', 'java.util.List', 'java.util.Map'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| DataSetDetailOutputModel | class |  |



## Class DataSetDetailOutputModel

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | DataSetDetailOutputModel |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
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

### Method List

| Name  | Type  | Description |
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




