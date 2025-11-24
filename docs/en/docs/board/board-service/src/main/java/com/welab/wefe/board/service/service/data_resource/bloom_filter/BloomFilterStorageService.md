# Basic Information

|      |      |
|------|------|
| Name | BloomFilterStorageService |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/data_resource/bloom_filter/BloomFilterStorageService.java |
| Package Name | com.welab.wefe.board.service.service.data_resource.bloom_filter |
| Dependencies | ['com.alibaba.fastjson.JSON', 'com.welab.wefe.board.service.service.AbstractService', 'com.welab.wefe.common.data.storage.common.Constant', 'com.welab.wefe.common.data.storage.model.DataItemModel', 'com.welab.wefe.common.data.storage.model.PageInputModel', 'com.welab.wefe.common.data.storage.model.PageOutputModel', 'com.welab.wefe.common.data.storage.service.persistent.PersistentStorage', 'com.welab.wefe.common.util.StringUtil', 'org.springframework.stereotype.Service', 'java.util.ArrayList', 'java.util.Collection', 'java.util.List', 'java.util.stream.Collectors'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| BloomFilterStorageService | class |  |



## Class BloomFilterStorageService

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | BloomFilterStorageService |
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
| saveList | void |  |
| getList | List<DataItemModel> |  |
| saveDataRow | void |  |
| previewBloomfilter | List<List<String>> |  |
| getListByPage | PageOutputModel |  |
| containsKey | boolean |  |
| buildDataItemModel | DataItemModel<String, String> |  |
| createRawBloomfilterTableName | String |  |
| saveHeaderRow | void |  |
| saveDataRows | void |  |
| save | void |  |
| save | void |  |
| deleteBloomfilter | void |  |
| count | int |  |
| count | int |  |
| getAddBatchSize | int |  |




