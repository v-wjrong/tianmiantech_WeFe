# 基础信息

|      |      |
|------|------|
| 名称 | FusionResultStorageService |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/fusion/FusionResultStorageService.java |
| 包名 | com.welab.wefe.board.service.service.fusion |
| 依赖项 | ['java.sql.SQLException', 'java.util.ArrayList', 'java.util.Collection', 'java.util.List', 'java.util.Set', 'java.util.stream.Collectors', 'org.springframework.stereotype.Service', 'com.alibaba.fastjson.JSON', 'com.welab.wefe.board.service.service.AbstractService', 'com.welab.wefe.common.data.storage.common.Constant', 'com.welab.wefe.common.data.storage.model.DataItemModel', 'com.welab.wefe.common.data.storage.model.PageInputModel', 'com.welab.wefe.common.data.storage.model.PageOutputModel', 'com.welab.wefe.common.data.storage.service.persistent.PersistentStorage', 'com.welab.wefe.common.util.StringUtil'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| FusionResultStorageService | class |  |



## 类 FusionResultStorageService

|      |      |
|------|------|
| 访问范围 | @Service;public |
| 类型 | class |
| 名称 | FusionResultStorageService |
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




