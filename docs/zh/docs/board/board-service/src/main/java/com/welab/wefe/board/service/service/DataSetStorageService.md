# 基础信息

|      |      |
|------|------|
| 名称 | DataSetStorageService |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/DataSetStorageService.java |
| 包名 | com.welab.wefe.board.service.service |
| 依赖项 | ['com.alibaba.fastjson.JSON', 'com.welab.wefe.common.data.storage.common.Constant', 'com.welab.wefe.common.data.storage.model.DataItemModel', 'com.welab.wefe.common.data.storage.model.PageInputModel', 'com.welab.wefe.common.data.storage.model.PageOutputModel', 'com.welab.wefe.common.data.storage.service.persistent.PersistentStorage', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.wefe.dto.global_config.storage.ClickHouseStorageConfigModel', 'com.welab.wefe.common.wefe.dto.global_config.storage.StorageBaseConfigModel', 'com.welab.wefe.common.wefe.dto.storage.ClickhouseConfig', 'com.welab.wefe.common.wefe.enums.GatewayProcessorType', 'org.springframework.stereotype.Service', 'java.util.ArrayList', 'java.util.Collection', 'java.util.List', 'java.util.stream.Collectors'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| DataSetStorageService | class |  |



## 类 DataSetStorageService

|      |      |
|------|------|
| 访问范围 | @Service;public |
| 类型 | class |
| 名称 | DataSetStorageService |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| DATABASE_NAME = Constant.DBName.WEFE_DATA | String |  |

### 方法列表

| 名称  | 类型  | 说明 |
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




