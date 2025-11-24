# Basic Information

|      |      |
|------|------|
| Name | FusionResultStorageService |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/fusion/FusionResultStorageService.java |
| Package Name | com.welab.wefe.board.service.service.fusion |
| Dependencies | ['java.sql.SQLException', 'java.util.ArrayList', 'java.util.Collection', 'java.util.List', 'java.util.Set', 'java.util.stream.Collectors', 'org.springframework.stereotype.Service', 'com.alibaba.fastjson.JSON', 'com.welab.wefe.board.service.service.AbstractService', 'com.welab.wefe.common.data.storage.common.Constant', 'com.welab.wefe.common.data.storage.model.DataItemModel', 'com.welab.wefe.common.data.storage.model.PageInputModel', 'com.welab.wefe.common.data.storage.model.PageOutputModel', 'com.welab.wefe.common.data.storage.service.persistent.PersistentStorage', 'com.welab.wefe.common.util.StringUtil'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| FusionResultStorageService | class |  |



## Class FusionResultStorageService

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | FusionResultStorageService |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| DATABASE_NAME = Constant.DBName.WEFE_DATA | String |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| buildDataItemModel | DataItemModel<String, String> |  |
| previewDataSet | List<List<String>> |  |
| isExists | Boolean |  |
| getByKey | DataItemModel |  |
| createRawDataSetHeaderTableName | String |  |
| count | int |  |
| getList | List<DataItemModel> |  |
| getAddBatchSize | int |  |
| createRawDataSetTableName | String |  |
| save | void |  |
| save | void |  |
| saveHeaderRow | void |  |
| saveDataRow | void |  |
| deleteDataSet | void |  |
| saveList | void |  |
| previewDataSet | List<List<String>> |  |
| count | int |  |
| containsKey | boolean |  |
| saveDataRows | void |  |




