# Basic Information

|      |      |
|------|------|
| Name | JobService |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/JobService.java |
| Package Name | com.welab.wefe.board.service.service |
| Dependencies | ['com.welab.wefe.board.service.api.project.job.UpdateJobStatusApi', 'com.welab.wefe.board.service.database.entity.job.JobMySqlModel', 'com.welab.wefe.board.service.database.entity.job.ProjectFlowMySqlModel', 'com.welab.wefe.board.service.database.entity.job.ProjectMySqlModel', 'com.welab.wefe.board.service.database.entity.job.TaskMySqlModel', 'com.welab.wefe.board.service.database.repository.JobMemberRepository', 'com.welab.wefe.board.service.database.repository.JobRepository', 'com.welab.wefe.board.service.database.repository.TaskRepository', 'com.welab.wefe.board.service.model.FlowGraph', 'com.welab.wefe.board.service.model.FlowGraphNode', 'com.welab.wefe.common.data.mysql.Where', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.web.util.CurrentAccountUtil', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'com.welab.wefe.common.wefe.enums.JobStatus', 'com.welab.wefe.common.wefe.enums.TaskStatus', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.data.jpa.domain.Specification', 'org.springframework.stereotype.Service', 'java.util', 'java.util.function.Function', 'java.util.stream.Collectors'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| JobService | class |  |



## Class JobService

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | JobService |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| taskRepo | TaskRepository |  |
| jobMemberService | JobMemberService |  |
| projectService | ProjectService |  |
| projectFlowNodeService | ProjectFlowNodeService |  |
| projectFlowService | ProjectFlowService |  |
| jobMemberRepo | JobMemberRepository |  |
| jobRepo | JobRepository |  |
| taskService | TaskService |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| updateJobStatus | void |  |
| runningJobCount | int |  |
| setGraphHasCacheResult | void |  |
| findByJobId | JobMySqlModel |  |
| updateJob | void |  |
| createFlowGraph | FlowGraph |  |
| listByJobId | List<JobMySqlModel> |  |
| checkCacheEnableStatus | void |  |




