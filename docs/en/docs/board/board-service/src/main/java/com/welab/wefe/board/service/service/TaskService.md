# Basic Information

|      |      |
|------|------|
| Name | TaskService |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/TaskService.java |
| Package Name | com.welab.wefe.board.service.service |
| Dependencies | ['com.welab.wefe.board.service.api.project.flow.QueryDataIoTaskConfigApi', 'com.welab.wefe.board.service.api.project.flow.QueryDataIoTaskFeaturesApi', 'com.welab.wefe.board.service.api.project.job.task.DetailApi', 'com.welab.wefe.board.service.component.OotComponent', 'com.welab.wefe.board.service.database.entity.job', 'com.welab.wefe.board.service.database.repository.JobRepository', 'com.welab.wefe.board.service.database.repository.TaskRepository', 'com.welab.wefe.board.service.dto.entity.DataIoTaskFeatureInfoOutputModel', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.data.mysql.Where', 'com.welab.wefe.common.data.mysql.enums.OrderBy', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.web.util.CurrentAccountUtil', 'com.welab.wefe.common.wefe.enums.ComponentType', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'com.welab.wefe.common.wefe.enums.TaskStatus', 'org.apache.commons.collections4.CollectionUtils', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.data.jpa.domain.Specification', 'org.springframework.stereotype.Service', 'java.util.ArrayList', 'java.util.Arrays', 'java.util.Collections', 'java.util.List', 'java.util.function.Function', 'java.util.stream.Collectors', 'java.util.stream.Stream'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| TaskService | class |  |



## Class TaskService

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | TaskService |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
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

### Method List

| Name  | Type  | Description |
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




