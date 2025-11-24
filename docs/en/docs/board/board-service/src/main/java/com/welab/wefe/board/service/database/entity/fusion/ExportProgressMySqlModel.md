# Basic Information

|      |      |
|------|------|
| Name | ExportProgressMySqlModel |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/database/entity/fusion/ExportProgressMySqlModel.java |
| Package Name | com.welab.wefe.board.service.database.entity.fusion |
| Dependencies | ['com.welab.wefe.board.service.database.entity.base.AbstractBaseMySqlModel', 'com.welab.wefe.board.service.fusion.enums.ExportStatus', 'javax.persistence.Entity', 'javax.persistence.EnumType', 'javax.persistence.Enumerated'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| ExportProgressMySqlModel | class |  |



## Class ExportProgressMySqlModel

|      |      |
|------|------|
| Access Modifier | @Entity(name = "fusion_result_export_progress");public |
| Type | class |
| Name | ExportProgressMySqlModel |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| status | ExportStatus |  |
| finishTime | long |  |
| businessId | String |  |
| progress | int |  |
| totalDataCount | int |  |
| processedCount | int |  |
| tableName | String |  |

### Method List

| Name  | Type  | Description |
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




