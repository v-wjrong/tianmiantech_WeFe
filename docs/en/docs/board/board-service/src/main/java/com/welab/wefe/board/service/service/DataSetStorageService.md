# Basic Information

|      |      |
|------|------|
| Name | DataSetStorageService |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/DataSetStorageService.java |
| Package Name | com.welab.wefe.board.service.service |
| Dependencies | ['com.alibaba.fastjson.JSON', 'com.welab.wefe.common.data.storage.common.Constant', 'com.welab.wefe.common.data.storage.model.DataItemModel', 'com.welab.wefe.common.data.storage.model.PageInputModel', 'com.welab.wefe.common.data.storage.model.PageOutputModel', 'com.welab.wefe.common.data.storage.service.persistent.PersistentStorage', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.wefe.dto.global_config.storage.ClickHouseStorageConfigModel', 'com.welab.wefe.common.wefe.dto.global_config.storage.StorageBaseConfigModel', 'com.welab.wefe.common.wefe.dto.storage.ClickhouseConfig', 'com.welab.wefe.common.wefe.enums.GatewayProcessorType', 'org.springframework.stereotype.Service', 'java.util.ArrayList', 'java.util.Collection', 'java.util.List', 'java.util.stream.Collectors'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| DataSetStorageService | class |  |



## Class DataSetStorageService

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | DataSetStorageService |
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
| count | int |  |
| getAddBatchSize | int |  |
| getByKey | DataItemModel |  |
| saveDataRow | void |  |
| initStorage | void |  |
| saveDataRows | void |  |
| getListByPage | PageOutputModel |  |
| saveList | void |  |
| containsKey | boolean |  |
| getList | List<DataItemModel> |  |
| saveHeaderRow | void |  |
| deleteDataSet | void |  |
| save | void |  |
| save | void |  |
| buildDataItemModel | DataItemModel<String, String> |  |
| previewDataSet | List<List<String>> |  |
| createRawDataSetTableName | String |  |
| count | int |  |




