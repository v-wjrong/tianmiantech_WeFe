# 基础信息

|      |      |
|------|------|
| 名称 | ExportProgressMySqlModel |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/database/entity/fusion/ExportProgressMySqlModel.java |
| 包名 | com.welab.wefe.board.service.database.entity.fusion |
| 依赖项 | ['com.welab.wefe.board.service.database.entity.base.AbstractBaseMySqlModel', 'com.welab.wefe.board.service.fusion.enums.ExportStatus', 'javax.persistence.Entity', 'javax.persistence.EnumType', 'javax.persistence.Enumerated'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| ExportProgressMySqlModel | class |  |



## 类 ExportProgressMySqlModel

|      |      |
|------|------|
| 访问范围 | @Entity(name = "fusion_result_export_progress");public |
| 类型 | class |
| 名称 | ExportProgressMySqlModel |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| status | ExportStatus |  |
| finishTime | long |  |
| businessId | String |  |
| progress | int |  |
| totalDataCount | int |  |
| processedCount | int |  |
| tableName | String |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getProcessedCount | int |  |
| getStatus | ExportStatus |  |
| setTotalDataCount | void |  |
| getTotalDataCount | int |  |
| setProgress | void |  |
| setProcessedCount | void |  |
| setBusinessId | void |  |
| getTableName | String |  |
| getProgress | int |  |
| getBusinessId | String |  |
| setTableName | void |  |
| setFinishTime | void |  |
| getFinishTime | long |  |
| setStatus | void |  |




