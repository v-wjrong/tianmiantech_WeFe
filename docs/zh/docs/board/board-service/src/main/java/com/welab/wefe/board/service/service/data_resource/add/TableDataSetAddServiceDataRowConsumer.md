# 基础信息

|      |      |
|------|------|
| 名称 | TableDataSetAddServiceDataRowConsumer |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/data_resource/add/TableDataSetAddServiceDataRowConsumer.java |
| 包名 | com.welab.wefe.board.service.service.data_resource.add |
| 依赖项 | ['com.welab.wefe.board.service.dto.vo.data_set.table_data_set.LabelDistribution', 'com.welab.wefe.board.service.service.DataSetStorageService', 'com.welab.wefe.board.service.service.data_resource.DataResourceUploadTaskService', 'com.welab.wefe.board.service.util.AbstractTableDataSetReader', 'com.welab.wefe.board.service.util.unique.AbstractDataSetUniqueFilter', 'com.welab.wefe.board.service.util.unique.ContainResult', 'com.welab.wefe.board.service.util.unique.DataSetBloomUniqueFilter', 'com.welab.wefe.board.service.util.unique.DataSetMemoryUniqueFilter', 'com.welab.wefe.common.BatchConsumer', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.ListUtil', 'com.welab.wefe.common.web.Launcher', 'org.apache.commons.collections4.CollectionUtils', 'org.eclipse.jetty.util.ConcurrentHashSet', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.math.BigDecimal', 'java.math.RoundingMode', 'java.util', 'java.util.concurrent.ConcurrentHashMap', 'java.util.concurrent.atomic.AtomicLong', 'java.util.concurrent.atomic.LongAdder', 'java.util.function.Consumer'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| TableDataSetAddServiceDataRowConsumer | class |  |



## 类 TableDataSetAddServiceDataRowConsumer

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | TableDataSetAddServiceDataRowConsumer |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
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

### 方法列表

| 名称  | 类型  | 说明 |
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




