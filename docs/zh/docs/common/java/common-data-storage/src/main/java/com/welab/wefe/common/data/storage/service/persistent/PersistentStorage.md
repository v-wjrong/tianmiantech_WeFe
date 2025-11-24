# 基础信息

|      |      |
|------|------|
| 名称 | PersistentStorage |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-data-storage/src/main/java/com/welab/wefe/common/data/storage/service/persistent/PersistentStorage.java |
| 包名 | com.welab.wefe.common.data.storage.service.persistent |
| 依赖项 | ['com.alibaba.druid.pool.DruidDataSource', 'com.welab.wefe.common.data.storage.model.DataItemModel', 'com.welab.wefe.common.data.storage.model.PageInputModel', 'com.welab.wefe.common.data.storage.model.PageOutputModel', 'com.welab.wefe.common.data.storage.service.persistent.clickhouse.ClickhouseStorage', 'com.welab.wefe.common.data.storage.service.persistent.mysql.MysqlConfig', 'com.welab.wefe.common.data.storage.service.persistent.mysql.MysqlStorage', 'com.welab.wefe.common.wefe.dto.storage.ClickhouseConfig', 'com.welab.wefe.common.wefe.dto.storage.DataSourceConfig', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.sql', 'java.util.List'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| PersistentStorage | class |  |



## 类 PersistentStorage

|      |      |
|------|------|
| 访问范围 | public abstract |
| 类型 | class |
| 名称 | PersistentStorage |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| dataSource | DruidDataSource |  |
| storage | PersistentStorage |  |
| log = LoggerFactory.getLogger(PersistentStorage.class) | Logger |  |
| inited = false | boolean |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| isExists | boolean |  |
| putAll | void |  |
| getByStream | void |  |
| init | boolean |  |
| getAddBatchSize | int |  |
| take | List<DataItemModel> |  |
| getPageBytes | PageOutputModel<byte[], byte[]> |  |
| getCountByByteSize | int |  |
| checkTbStream | void |  |
| get | DataItemModel |  |
| checkTB | void |  |
| collect | List<DataItemModel> |  |
| init | boolean |  |
| count | int |  |
| checkConnection | void |  |
| dropDB | void |  |
| close | void |  |
| getPage | PageOutputModel |  |
| formatTableName | String |  |
| main | void |  |
| delete | void |  |
| buildDruidDataSource | DruidDataSource |  |
| getInstance | PersistentStorage |  |
| putAllNew | void |  |
| collectBytes | List<DataItemModel<byte[], byte[]>> |  |
| validationQuery | String |  |
| dropTB | void |  |
| close | void |  |
| inited | boolean |  |
| getConnection | Connection |  |
| put | void |  |




