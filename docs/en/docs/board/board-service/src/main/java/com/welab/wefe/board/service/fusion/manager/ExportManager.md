# Basic Information

|      |      |
|------|------|
| Name | ExportManager |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/fusion/manager/ExportManager.java |
| Package Name | com.welab.wefe.board.service.fusion.manager |
| Dependencies | ['com.welab.wefe.board.service.database.entity.fusion.ExportProgressMySqlModel', 'com.welab.wefe.board.service.dto.fusion.FusionResultExportProgress', 'com.welab.wefe.board.service.service.fusion.ExportProgressService', 'com.welab.wefe.common.web.Launcher', 'com.welab.wefe.common.web.util.ModelMapper', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.util.concurrent.ConcurrentHashMap'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| ExportManager | class |  |



## Class ExportManager

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | ExportManager |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| LOG = LoggerFactory.getLogger(ActuatorManager.class) | Logger |  |
| EXPORT_TASK = new ConcurrentHashMap<>() | ConcurrentHashMap<String, FusionResultExportProgress> |  |
| exportProgressService | ExportProgressService |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| set | void |  |
| get | FusionResultExportProgress |  |
| romove | void |  |




