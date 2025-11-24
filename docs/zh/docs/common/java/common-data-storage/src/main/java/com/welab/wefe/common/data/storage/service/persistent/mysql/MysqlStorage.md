# 基础信息

|      |      |
|------|------|
| 名称 | MysqlStorage |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-data-storage/src/main/java/com/welab/wefe/common/data/storage/service/persistent/mysql/MysqlStorage.java |
| 包名 | com.welab.wefe.common.data.storage.service.persistent.mysql |
| 依赖项 | ['com.welab.wefe.common.data.storage.model.DataItemModel', 'com.welab.wefe.common.data.storage.model.PageInputModel', 'com.welab.wefe.common.data.storage.model.PageOutputModel', 'com.welab.wefe.common.data.storage.service.persistent.PersistentStorage', 'java.sql.SQLException', 'java.util.List'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| MysqlStorage | class |  |



## 类 MysqlStorage

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | MysqlStorage |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| config | MysqlConfig |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| dropDB | void |  |
| take | List<DataItemModel> |  |
| delete | void |  |
| put | void |  |
| count | int |  |
| collectBytes | List<DataItemModel<byte[], byte[]>> |  |
| collect | List<DataItemModel> |  |
| getAddBatchSize | int |  |
| getPageBytes | PageOutputModel<byte[], byte[]> |  |
| dropTB | void |  |
| putAll | void |  |
| getPage | PageOutputModel |  |
| get | DataItemModel |  |
| isExists | boolean |  |
| validationQuery | String |  |




