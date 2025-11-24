# 基础信息

|      |      |
|------|------|
| 名称 | TaskService |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/TaskService.java |
| 包名 | com.welab.wefe.board.service.service |
| 依赖项 | ['com.welab.wefe.board.service.api.project.flow.QueryDataIoTaskConfigApi', 'com.welab.wefe.board.service.api.project.flow.QueryDataIoTaskFeaturesApi', 'com.welab.wefe.board.service.api.project.job.task.DetailApi', 'com.welab.wefe.board.service.component.OotComponent', 'com.welab.wefe.board.service.database.entity.job', 'com.welab.wefe.board.service.database.repository.JobRepository', 'com.welab.wefe.board.service.database.repository.TaskRepository', 'com.welab.wefe.board.service.dto.entity.DataIoTaskFeatureInfoOutputModel', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.data.mysql.Where', 'com.welab.wefe.common.data.mysql.enums.OrderBy', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.web.util.CurrentAccountUtil', 'com.welab.wefe.common.wefe.enums.ComponentType', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'com.welab.wefe.common.wefe.enums.TaskStatus', 'org.apache.commons.collections4.CollectionUtils', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.data.jpa.domain.Specification', 'org.springframework.stereotype.Service', 'java.util.ArrayList', 'java.util.Arrays', 'java.util.Collections', 'java.util.List', 'java.util.function.Function', 'java.util.stream.Collectors', 'java.util.stream.Stream'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| TaskService | class |  |



## 类 TaskService

|      |      |
|------|------|
| 访问范围 | @Service;public |
| 类型 | class |
| 名称 | TaskService |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| projectFlowService | ProjectFlowService |  |
| jobService | JobService |  |
| taskRepo | TaskRepository |  |
| LOG = LoggerFactory.getLogger(this.getClass()) | Logger |  |
| gatewayService | GatewayService |  |
| jobRepository | JobRepository |  |
| projectFlowNodeService | ProjectFlowNodeService |  |
| projectService | ProjectService |  |
| jobMemberService | JobMemberService |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| findTotalParentTaskMysqlModelList | void |  |
| findAll | List<TaskMySqlModel> |  |
| findDataIoTask | TaskMySqlModel |  |
| findByParentTaskId | TaskMySqlModel |  |
| findDataIoTaskFeatures | List<DataIoTaskFeatureInfoOutputModel> |  |
| findOne | TaskMySqlModel |  |
| findDataIoTaskConfig | JObject |  |
| listByJobId | List<TaskMySqlModel> |  |
| findOne | TaskMySqlModel |  |
| updateTask | TaskMySqlModel |  |
| findAll | List<TaskMySqlModel> |  |
| findAll | List<TaskMySqlModel> |  |
| findDataIoTaskFeaturesWithOot | List<DataIoTaskFeatureInfoOutputModel> |  |
| findAll | List<TaskMySqlModel> |  |
| findOne | TaskMySqlModel |  |
| findHomologousBranchByJobId | List<TaskMySqlModel> |  |
| listTaskWithGridSearch | List<TaskMySqlModel> |  |
| baseFindHomologousBranch | List<TaskMySqlModel> |  |
| findTaskHistory | List<TaskMySqlModel> |  |
| findDataIoTaskFeaturesWithNonOot | List<DataIoTaskFeatureInfoOutputModel> |  |
| findTotalSubTaskMysqlModelList | void |  |




