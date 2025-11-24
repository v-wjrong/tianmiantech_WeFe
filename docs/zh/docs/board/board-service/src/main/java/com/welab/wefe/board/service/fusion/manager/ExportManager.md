# 基础信息

|      |      |
|------|------|
| 名称 | ExportManager |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/fusion/manager/ExportManager.java |
| 包名 | com.welab.wefe.board.service.fusion.manager |
| 依赖项 | ['com.welab.wefe.board.service.database.entity.fusion.ExportProgressMySqlModel', 'com.welab.wefe.board.service.dto.fusion.FusionResultExportProgress', 'com.welab.wefe.board.service.service.fusion.ExportProgressService', 'com.welab.wefe.common.web.Launcher', 'com.welab.wefe.common.web.util.ModelMapper', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.util.concurrent.ConcurrentHashMap'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| ExportManager | class |  |



## 类 ExportManager

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | ExportManager |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| LOG = LoggerFactory.getLogger(ActuatorManager.class) | Logger |  |
| EXPORT_TASK = new ConcurrentHashMap<>() | ConcurrentHashMap<String, FusionResultExportProgress> |  |
| exportProgressService | ExportProgressService |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| set | void |  |
| get | FusionResultExportProgress |  |
| romove | void |  |




