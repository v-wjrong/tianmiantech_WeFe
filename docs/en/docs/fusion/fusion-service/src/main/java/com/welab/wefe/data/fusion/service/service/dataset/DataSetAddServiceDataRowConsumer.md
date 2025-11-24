# Basic Information

|      |      |
|------|------|
| Name | DataSetAddServiceDataRowConsumer |
| Language | .java |
| Code Path | WeFe/fusion/fusion-service/src/main/java/com/welab/wefe/data/fusion/service/service/dataset/DataSetAddServiceDataRowConsumer.java |
| Package Name | com.welab.wefe.data.fusion.service.service.dataset |
| Dependencies | ['com.welab.wefe.common.BatchConsumer', 'com.welab.wefe.common.web.Launcher', 'com.welab.wefe.data.fusion.service.database.entity.DataSetMySqlModel', 'com.welab.wefe.data.fusion.service.database.repository.DataSetRepository', 'com.welab.wefe.data.fusion.service.enums.Progress', 'java.io.File', 'java.util.List', 'java.util.Map', 'java.util.concurrent.atomic.LongAdder', 'java.util.function.Consumer'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| DataSetAddServiceDataRowConsumer | class |  |



## Class DataSetAddServiceDataRowConsumer

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | DataSetAddServiceDataRowConsumer |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| repeatDataCount = new LongAdder() | LongAdder |  |
| rowCountFromDB | long |  |
| rows | List<String> |  |
| batchConsumer | BatchConsumer<Map<String, Object>> |  |
| dataSetId | String |  |
| file | File |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| waitForFinishAndClose | void |  |
| saveDataRows | void |  |
| accept | void |  |




