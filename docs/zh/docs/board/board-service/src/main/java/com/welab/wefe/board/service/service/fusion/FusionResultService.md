# 基础信息

|      |      |
|------|------|
| 名称 | FusionResultService |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/fusion/FusionResultService.java |
| 包名 | com.welab.wefe.board.service.service.fusion |
| 依赖项 | ['java.util.ArrayList', 'java.util.Date', 'java.util.Iterator', 'java.util.List', 'java.util.concurrent.ExecutorService', 'java.util.concurrent.Executors', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.stereotype.Service', 'com.google.common.collect.Lists', 'com.welab.wefe.board.service.api.project.fusion.result.ResultExportApi', 'com.welab.wefe.board.service.database.entity.fusion.FusionTaskMySqlModel', 'com.welab.wefe.board.service.dto.fusion.FusionResultExportProgress', 'com.welab.wefe.board.service.fusion.enums.ExportStatus', 'com.welab.wefe.board.service.fusion.manager.ExportManager', 'com.welab.wefe.board.service.service.AbstractService', 'com.welab.wefe.common.CommonThreadPool', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.data.storage.common.Constant', 'com.welab.wefe.common.data.storage.model.DataItemModel', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.jdbc.JdbcClient', 'com.welab.wefe.common.util.DateUtil', 'com.welab.wefe.common.util.StringUtil'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| FusionResultService | class |  |



## 类 FusionResultService

|      |      |
|------|------|
| 访问范围 | @Service;public |
| 类型 | class |
| 名称 | FusionResultService |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| fusionResultStorageService | FusionResultStorageService |  |
| fusionTaskService | FusionTaskService |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| export | String |  |
| writer | void |  |
| create | void |  |
| writerBatch | void |  |
| partitionList | List<List<T>> |  |




