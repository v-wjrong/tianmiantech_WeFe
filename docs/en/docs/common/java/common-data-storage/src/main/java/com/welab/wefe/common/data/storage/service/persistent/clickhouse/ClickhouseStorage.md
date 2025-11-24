# Basic Information

|      |      |
|------|------|
| Name | ClickhouseStorage |
| Language | .java |
| Code Path | WeFe/common/java/common-data-storage/src/main/java/com/welab/wefe/common/data/storage/service/persistent/clickhouse/ClickhouseStorage.java |
| Package Name | com.welab.wefe.common.data.storage.service.persistent.clickhouse |
| Dependencies | ['com.welab.wefe.common.data.storage.model.DataItemModel', 'com.welab.wefe.common.data.storage.model.PageInputModel', 'com.welab.wefe.common.data.storage.model.PageOutputModel', 'com.welab.wefe.common.data.storage.service.persistent.PersistentStorage', 'com.welab.wefe.common.data.storage.service.persistent.PersistentStorageStreamHandler', 'com.welab.wefe.common.wefe.dto.storage.ClickhouseConfig', 'net.razorvine.pickle.Pickler', 'net.razorvine.pickle.Unpickler', 'java.math.BigDecimal', 'java.math.RoundingMode', 'java.sql', 'java.util.ArrayList', 'java.util.List', 'java.util.UUID'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| ClickhouseStorage | class |  |



## Class ClickhouseStorage

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | ClickhouseStorage |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| config | ClickhouseConfig |  |

### Method List

| Name  | Type  | Description |
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




