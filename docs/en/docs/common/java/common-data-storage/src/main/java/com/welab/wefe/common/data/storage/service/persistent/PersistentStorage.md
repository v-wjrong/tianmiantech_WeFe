# Basic Information

|      |      |
|------|------|
| Name | PersistentStorage |
| Language | .java |
| Code Path | WeFe/common/java/common-data-storage/src/main/java/com/welab/wefe/common/data/storage/service/persistent/PersistentStorage.java |
| Package Name | com.welab.wefe.common.data.storage.service.persistent |
| Dependencies | ['com.alibaba.druid.pool.DruidDataSource', 'com.welab.wefe.common.data.storage.model.DataItemModel', 'com.welab.wefe.common.data.storage.model.PageInputModel', 'com.welab.wefe.common.data.storage.model.PageOutputModel', 'com.welab.wefe.common.data.storage.service.persistent.clickhouse.ClickhouseStorage', 'com.welab.wefe.common.data.storage.service.persistent.mysql.MysqlConfig', 'com.welab.wefe.common.data.storage.service.persistent.mysql.MysqlStorage', 'com.welab.wefe.common.wefe.dto.storage.ClickhouseConfig', 'com.welab.wefe.common.wefe.dto.storage.DataSourceConfig', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.sql', 'java.util.List'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| PersistentStorage | class |  |



## Class PersistentStorage

|      |      |
|------|------|
| Access Modifier | public abstract |
| Type | class |
| Name | PersistentStorage |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| dataSource | DruidDataSource |  |
| storage | PersistentStorage |  |
| log = LoggerFactory.getLogger(PersistentStorage.class) | Logger |  |
| inited = false | boolean |  |

### Method List

| Name  | Type  | Description |
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




