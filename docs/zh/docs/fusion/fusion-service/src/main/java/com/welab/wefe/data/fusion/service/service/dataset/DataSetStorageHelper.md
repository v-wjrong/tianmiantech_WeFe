# 基础信息

|      |      |
|------|------|
| 名称 | DataSetStorageHelper |
| 编码语言 | .java |
| 代码路径 | WeFe/fusion/fusion-service/src/main/java/com/welab/wefe/data/fusion/service/service/dataset/DataSetStorageHelper.java |
| 包名 | com.welab.wefe.data.fusion.service.service.dataset |
| 依赖项 | ['com.welab.wefe.common.web.Launcher', 'com.welab.wefe.data.fusion.service.database.entity.DataSetMySqlModel', 'com.welab.wefe.data.fusion.service.database.repository.DataSetRepository', 'com.welab.wefe.data.fusion.service.enums.Progress', 'com.welab.wefe.data.fusion.service.service.DataStorageService', 'java.util.Date', 'java.util.List', 'java.util.Map'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| DataSetStorageHelper | class |  |



## 类 DataSetStorageHelper

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | DataSetStorageHelper |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| dataStorageService | DataStorageService |  |
| process | Progress |  |
| DATA_SET_TABLE_PRE = "data_fusion_" | String |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| insertDataSet | void |  |
| createDataSetTable | void |  |
| createRawDataSetTableName | String |  |
| saveDataSetRows | void |  |
| countDataSetRows | int |  |




