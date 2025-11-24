# 基础信息

|      |      |
|------|------|
| 名称 | ClickhouseStorage |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-data-storage/src/main/java/com/welab/wefe/common/data/storage/service/persistent/clickhouse/ClickhouseStorage.java |
| 包名 | com.welab.wefe.common.data.storage.service.persistent.clickhouse |
| 依赖项 | ['com.welab.wefe.common.data.storage.model.DataItemModel', 'com.welab.wefe.common.data.storage.model.PageInputModel', 'com.welab.wefe.common.data.storage.model.PageOutputModel', 'com.welab.wefe.common.data.storage.service.persistent.PersistentStorage', 'com.welab.wefe.common.data.storage.service.persistent.PersistentStorageStreamHandler', 'com.welab.wefe.common.wefe.dto.storage.ClickhouseConfig', 'net.razorvine.pickle.Pickler', 'net.razorvine.pickle.Unpickler', 'java.math.BigDecimal', 'java.math.RoundingMode', 'java.sql', 'java.util.ArrayList', 'java.util.List', 'java.util.UUID'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| ClickhouseStorage | class |  |



## 类 ClickhouseStorage

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | ClickhouseStorage |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| config | ClickhouseConfig |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| dropTB | void |  |
| getAddBatchSize | int |  |
| delete | void |  |
| put | void |  |
| count | int |  |
| collect | List<DataItemModel> |  |
| get | DataItemModel |  |
| putAll | void |  |
| collectBytes | List<DataItemModel<byte[], byte[]>> |  |
| getPage | PageOutputModel |  |
| take | List<DataItemModel> |  |
| getPageBytes | PageOutputModel<byte[], byte[]> |  |
| dropDB | void |  |
| getCountByByteSize | int |  |
| isExists | boolean |  |
| validationQuery | String |  |
| putAllNew | void |  |
| getByStream | void |  |




