# 基础信息

|      |      |
|------|------|
| 名称 | BloomFilterStorageService |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/data_resource/bloom_filter/BloomFilterStorageService.java |
| 包名 | com.welab.wefe.board.service.service.data_resource.bloom_filter |
| 依赖项 | ['com.alibaba.fastjson.JSON', 'com.welab.wefe.board.service.service.AbstractService', 'com.welab.wefe.common.data.storage.common.Constant', 'com.welab.wefe.common.data.storage.model.DataItemModel', 'com.welab.wefe.common.data.storage.model.PageInputModel', 'com.welab.wefe.common.data.storage.model.PageOutputModel', 'com.welab.wefe.common.data.storage.service.persistent.PersistentStorage', 'com.welab.wefe.common.util.StringUtil', 'org.springframework.stereotype.Service', 'java.util.ArrayList', 'java.util.Collection', 'java.util.List', 'java.util.stream.Collectors'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| BloomFilterStorageService | class |  |



## 类 BloomFilterStorageService

|      |      |
|------|------|
| 访问范围 | @Service;public |
| 类型 | class |
| 名称 | BloomFilterStorageService |
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




