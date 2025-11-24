# 基础信息

|      |      |
|------|------|
| 名称 | DataSetAddServiceDataRowConsumer |
| 编码语言 | .java |
| 代码路径 | WeFe/fusion/fusion-service/src/main/java/com/welab/wefe/data/fusion/service/service/dataset/DataSetAddServiceDataRowConsumer.java |
| 包名 | com.welab.wefe.data.fusion.service.service.dataset |
| 依赖项 | ['com.welab.wefe.common.BatchConsumer', 'com.welab.wefe.common.web.Launcher', 'com.welab.wefe.data.fusion.service.database.entity.DataSetMySqlModel', 'com.welab.wefe.data.fusion.service.database.repository.DataSetRepository', 'com.welab.wefe.data.fusion.service.enums.Progress', 'java.io.File', 'java.util.List', 'java.util.Map', 'java.util.concurrent.atomic.LongAdder', 'java.util.function.Consumer'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| DataSetAddServiceDataRowConsumer | class |  |



## 类 DataSetAddServiceDataRowConsumer

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | DataSetAddServiceDataRowConsumer |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| repeatDataCount = new LongAdder() | LongAdder |  |
| rowCountFromDB | long |  |
| rows | List<String> |  |
| batchConsumer | BatchConsumer<Map<String, Object>> |  |
| dataSetId | String |  |
| file | File |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| waitForFinishAndClose | void |  |
| saveDataRows | void |  |
| accept | void |  |




