# Basic Information

|      |      |
|------|------|
| Name | TableDataSetAddServiceDataRowConsumer |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/data_resource/add/TableDataSetAddServiceDataRowConsumer.java |
| Package Name | com.welab.wefe.board.service.service.data_resource.add |
| Dependencies | ['com.welab.wefe.board.service.dto.vo.data_set.table_data_set.LabelDistribution', 'com.welab.wefe.board.service.service.DataSetStorageService', 'com.welab.wefe.board.service.service.data_resource.DataResourceUploadTaskService', 'com.welab.wefe.board.service.util.AbstractTableDataSetReader', 'com.welab.wefe.board.service.util.unique.AbstractDataSetUniqueFilter', 'com.welab.wefe.board.service.util.unique.ContainResult', 'com.welab.wefe.board.service.util.unique.DataSetBloomUniqueFilter', 'com.welab.wefe.board.service.util.unique.DataSetMemoryUniqueFilter', 'com.welab.wefe.common.BatchConsumer', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.ListUtil', 'com.welab.wefe.common.web.Launcher', 'org.apache.commons.collections4.CollectionUtils', 'org.eclipse.jetty.util.ConcurrentHashSet', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.math.BigDecimal', 'java.math.RoundingMode', 'java.util', 'java.util.concurrent.ConcurrentHashMap', 'java.util.concurrent.atomic.AtomicLong', 'java.util.concurrent.atomic.LongAdder', 'java.util.function.Consumer'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| TableDataSetAddServiceDataRowConsumer | class |  |



## Class TableDataSetAddServiceDataRowConsumer

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | TableDataSetAddServiceDataRowConsumer |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| maxBatchSize = 0 | int |  |
| uniqueFilter | AbstractDataSetUniqueFilter |  |
| dataResourceUploadTaskService | DataResourceUploadTaskService |  |
| dataSetReader | AbstractTableDataSetReader |  |
| dataSetStorageService | DataSetStorageService |  |
| Y_COLUMN_NAME = "y" | String |  |
| firstColumnName | String |  |
| containsY | boolean |  |
| deduplication | boolean |  |
| yPositiveExampleCount = new AtomicLong(0) | AtomicLong |  |
| labelSet = new ConcurrentHashSet<>() | Set<String> |  |
| LOG = LoggerFactory.getLogger(TableDataSetAddServiceDataRowConsumer.class) | Logger |  |
| batchConsumer | BatchConsumer<List<Object>> |  |
| repeatDataCount = new LongAdder() | LongAdder |  |
| dataSetId | String |  |
| labelDistribution = new ConcurrentHashMap<>() | Map<String, Integer> |  |
| yIndex | int |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| accept | void |  |
| waitForFinishAndClose | void |  |
| moveY | void |  |
| getLabelDistribution | LabelDistribution |  |
| getRepeatDataCount | long |  |
| statisticPositiveExampleCount | void |  |
| getPositiveExampleRatio | double |  |
| createUniqueFilter | AbstractDataSetUniqueFilter |  |
| getPositiveExampleCount | long |  |
| saveRowWithDeduplication | void |  |




