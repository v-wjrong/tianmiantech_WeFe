# 基础信息

|      |      |
|------|------|
| 名称 | ModelOotRecordService |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/ModelOotRecordService.java |
| 包名 | com.welab.wefe.board.service.service |
| 依赖项 | ['com.welab.wefe.board.service.database.entity.job.ModelOotRecordMysqlModel', 'com.welab.wefe.board.service.database.repository.ModelOotRecordRepository', 'com.welab.wefe.common.data.mysql.Where', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.data.jpa.domain.Specification', 'org.springframework.stereotype.Service'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| ModelOotRecordService | class |  |



## 类 ModelOotRecordService

|      |      |
|------|------|
| 访问范围 | @Service;public |
| 类型 | class |
| 名称 | ModelOotRecordService |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| modelOotRecordRepository | ModelOotRecordRepository |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| save | void |  |
| findByFlowId | ModelOotRecordMysqlModel |  |
| findByJobIdAndModelFlowNodeId | ModelOotRecordMysqlModel |  |




