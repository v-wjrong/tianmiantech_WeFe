# Basic Information

|      |      |
|------|------|
| Name | MysqlStorage |
| Language | .java |
| Code Path | WeFe/common/java/common-data-storage/src/main/java/com/welab/wefe/common/data/storage/service/persistent/mysql/MysqlStorage.java |
| Package Name | com.welab.wefe.common.data.storage.service.persistent.mysql |
| Dependencies | ['com.welab.wefe.common.data.storage.model.DataItemModel', 'com.welab.wefe.common.data.storage.model.PageInputModel', 'com.welab.wefe.common.data.storage.model.PageOutputModel', 'com.welab.wefe.common.data.storage.service.persistent.PersistentStorage', 'java.sql.SQLException', 'java.util.List'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| MysqlStorage | class |  |



## Class MysqlStorage

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | MysqlStorage |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| config | MysqlConfig |  |

### Method List

| Name  | Type  | Description |
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




