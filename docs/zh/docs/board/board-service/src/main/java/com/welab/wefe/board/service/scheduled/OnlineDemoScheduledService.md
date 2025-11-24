# 基础信息

|      |      |
|------|------|
| 名称 | OnlineDemoScheduledService |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/scheduled/OnlineDemoScheduledService.java |
| 包名 | com.welab.wefe.board.service.scheduled |
| 依赖项 | ['com.welab.wefe.board.service.api.project.project.CloseProjectApi', 'com.welab.wefe.board.service.constant.Config', 'com.welab.wefe.board.service.database.entity.OperationLogMysqlModel', 'com.welab.wefe.board.service.database.entity.base.AbstractMySqlModel', 'com.welab.wefe.board.service.database.entity.job.ProjectMySqlModel', 'com.welab.wefe.board.service.database.repository.GlobalConfigRepository', 'com.welab.wefe.board.service.database.repository.ProjectRepository', 'com.welab.wefe.board.service.service.ProjectService', 'com.welab.wefe.common.TimeSpan', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.context.annotation.Lazy', 'org.springframework.scheduling.annotation.Scheduled', 'org.springframework.stereotype.Component', 'org.springframework.transaction.annotation.Transactional', 'javax.persistence.Entity', 'javax.persistence.Table', 'java.util.Date'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| OnlineDemoScheduledService | class |  |



## 类 OnlineDemoScheduledService

|      |      |
|------|------|
| 访问范围 | @Component;@Lazy(false);public |
| 类型 | class |
| 名称 | OnlineDemoScheduledService |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| projectRepository | ProjectRepository |  |
| globalConfigRepository | GlobalConfigRepository |  |
| projectService | ProjectService |  |
| LOG = LoggerFactory.getLogger(this.getClass()) | Logger |  |
| config | Config |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| clean | void |  |
| delete | void |  |




