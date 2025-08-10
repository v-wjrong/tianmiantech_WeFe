# Basic Information

|      |      |
|------|------|
| Name | FlowJobService |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/FlowJobService.java |
| Package Name | com.welab.wefe.board.service.service |
| Dependencies | ['com.welab.wefe.board.service.api.project.job.QueryApi', 'com.welab.wefe.board.service.database.entity.job.JobMySqlModel', 'com.welab.wefe.board.service.database.entity.job.ProjectFlowMySqlModel', 'com.welab.wefe.board.service.database.entity.job.ProjectMySqlModel', 'com.welab.wefe.board.service.database.entity.job.TaskMySqlModel', 'com.welab.wefe.board.service.database.repository.JobRepository', 'com.welab.wefe.board.service.dto.base.PagingOutput', 'com.welab.wefe.board.service.dto.entity.job.JobListOutputModel', 'com.welab.wefe.board.service.dto.entity.job.JobOutputModel', 'com.welab.wefe.board.service.dto.vo.JobProgressOutput', 'com.welab.wefe.common.data.mysql.Where', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.web.util.ModelMapper', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'com.welab.wefe.common.wefe.enums.JobStatus', 'com.welab.wefe.common.wefe.enums.TaskStatus', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.data.jpa.domain.Specification', 'org.springframework.stereotype.Service', 'java.util.List'] |
| Brief Description | The FlowJobService provides flow job management functionalities: paginated query of execution history (query), retrieving job details (detail), and progress tracking (getProgress). It relies on multiple services and repositories, returning corresponding data models through conditional filtering and status evaluation. |

# Description

FlowJobService is a service class that inherits from AbstractService and is used to manage the execution records, details, and progress queries of workflow jobs. It relies on components such as JobRepository, TaskService, ProjectFlowService, ProjectService, and JobService. Key functionalities include paginated querying of workflow execution history with job filtering based on conditions; retrieving job details, supporting queries via workflow ID or job ID; and obtaining job execution progress, which determines the current execution node based on job status and task status to return progress information. The progress query logic covers various status handling scenarios, including running, abnormal interruption, manual interruption, and not started.

# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| FlowJobService | class | The FlowJobService provides stream job management functionalities, including paginated querying of execution records, retrieving job details and progress. It relies on multiple services for data processing, supports filtering jobs based on conditions, and returns progress information according to status. |



## Class FlowJobService

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | FlowJobService |
| Description | The FlowJobService provides stream job management functionalities, including paginated querying of execution records, retrieving job details and progress. It relies on multiple services for data processing, supports filtering jobs based on conditions, and returns progress information according to status. |


### UML Class Diagram

```mermaid
classDiagram
    class FlowJobService {
        -JobRepository jobRepo
        -TaskService taskService
        -ProjectFlowService projectFlowService
        -ProjectService projectService
        -JobService jobService
        +PagingOutput~JobListOutputModel~ query(QueryApi$Input input)
        +JobOutputModel detail(String flowId, String jobId, JobMemberRole role)
        +JobProgressOutput getProgress(String jobId, JobMemberRole role)
    }

    class AbstractService {
        <<Abstract>>
    }

    class JobRepository {
        +PagingOutput~JobListOutputModel~ paging(Specification~JobMySqlModel~ where, QueryApi$Input input, Class~JobListOutputModel~ clazz)
        +JobMySqlModel findByJobId(String jobId, String role)
        +JobMySqlModel findLastByFlowId(String flowId, String role)
    }

    class TaskService {
        +List~TaskMySqlModel~ listByJobId(String jobId, JobMemberRole role)
    }

    class ProjectFlowService {
        +ProjectFlowMySqlModel findOne(String flowId)
    }

    class ProjectService {
        +ProjectMySqlModel findByProjectId(String projectId)
    }

    class JobService {
        +JobMySqlModel findByJobId(String jobId, JobMemberRole role)
    }

    class QueryApi {
        class Input {
            +String flowId
            +String jobId
            +String status
            +String name
        }
    }

    class JobListOutputModel
    class JobOutputModel
    class JobProgressOutput
    class JobMySqlModel
    class TaskMySqlModel
    class ProjectFlowMySqlModel
    class ProjectMySqlModel
    class JobMemberRole
    class JobStatus
    class TaskStatus

    FlowJobService --|> AbstractService : Inheritance
    FlowJobService --> JobRepository : Dependency
    FlowJobService --> TaskService : Dependency
    FlowJobService --> ProjectFlowService : Dependency
    FlowJobService --> ProjectService : Dependency
    FlowJobService --> JobService : Dependency
    FlowJobService --> QueryApi : Uses Input parameter
    JobRepository --> JobMySqlModel : Operates
    TaskService --> TaskMySqlModel : Operates
    ProjectFlowService --> ProjectFlowMySqlModel : Operates
    ProjectService --> ProjectMySqlModel : Operates
    JobService --> JobMySqlModel : Operates
    QueryApi$Input --> JobListOutputModel : Maps to
    JobProgressOutput --> JobMySqlModel : Contains
    JobProgressOutput --> TaskMySqlModel : Contains
```

Class Diagram Description:
FlowJobService is a service class that inherits from AbstractService, primarily handling operations related to flow jobs. It depends on multiple service classes (JobRepository, TaskService, etc.) and model classes (JobMySqlModel, TaskMySqlModel, etc.), providing functionalities such as querying job history, retrieving job details, and obtaining job progress. The class diagram clearly illustrates the inheritance, dependency, and association relationships between these classes, reflecting the layered architecture design of the system.


### Internal Method Call Graph

```mermaid
graph TD
    A["Class FlowJobService"]
    B["Property: JobRepository jobRepo"]
    C["Property: TaskService taskService"]
    D["Property: ProjectFlowService projectFlowService"]
    E["Property: ProjectService projectService"]
    F["Property: JobService jobService"]
    G["Method: query(QueryApi.Input input)"]
    H["Method: detail(String flowId, String jobId, JobMemberRole role)"]
    I["Method: getProgress(String jobId, JobMemberRole role)"]
    J["Subprocess: Build Specification conditions"]
    K["Invoke: jobRepo.paging"]
    L["Condition check: Is jobId null"]
    M["Invoke: projectFlowService.findOne"]
    N["Invoke: projectService.findByProjectId"]
    O["Invoke: jobRepo.findLastByFlowId"]
    P["Invoke: jobRepo.findByJobId"]
    Q["Invoke: ModelMapper.map"]
    R["Invoke: jobService.findByJobId"]
    S["Invoke: taskService.listByJobId"]
    T["Condition branch: Task status handling"]
    U["Stream processing: Filter running/error/stop/wait_run status tasks"]
    V["Return: JobProgressOutput.success"]

    A --> B
    A --> C
    A --> D
    A --> E
    A --> F
    A --> G
    A --> H
    A --> I
    G --> J --> K
    H --> L
    L --"Yes"--> M --> N --> O
    L --"No"--> P
    O & P --> Q
    I --> R --> S --> T
    T --"success"--> "Take last task"
    T --"wait_run"--> "Return null"
    T --"Other statuses"--> U --> V
```

Flowchart description: This flowchart illustrates three core methods of the FlowJobService class. The query method performs paginated queries by constructing Specification conditions; the detail method queries either the latest flow task or a specified task based on whether jobId is null, ultimately mapping to an output model; the getProgress method determines task progress through multi-level status checks (including running, error, stopped, etc.), incorporating complex stream filtering logic. Each method combines different repository and service calls to complete business logic, demonstrating the processing of task state machines.

### Field List

| Name  | Type  | Description |
|-------|-------|------|
| projectFlowService | ProjectFlowService | Automatically inject the ProjectFlowService instance. |
| jobRepo | JobRepository | Automatically inject the JobRepository instance into the jobRepo variable. |
| jobService | JobService | Automatically inject JobService instances. |
| projectService | ProjectService | Using @Autowired to automatically inject an instance of ProjectService. |
| taskService | TaskService | Using @Autowired to automatically inject a TaskService instance. |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| query | PagingOutput<JobListOutputModel> | This method queries the task list based on input conditions, constructing query criteria through flow ID, task ID, status, non-arbitrator role, and fuzzy name matching, and returns paginated results. |
| detail | JobOutputModel | This method retrieves task details based on the process ID and task ID. If no task ID is provided, it queries the last task of the process; otherwise, it queries according to the specified task ID. Returns the task details or null. |
| getProgress | JobProgressOutput | Get Task Progress: Query task status based on task ID and role, returning task and current execution node information. Handles states such as successful processing, pending execution, and abnormal interruptions to ensure accurate results. |




