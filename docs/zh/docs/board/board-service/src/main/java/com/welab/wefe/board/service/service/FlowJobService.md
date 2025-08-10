# 基础信息

|      |      |
|------|------|
| 名称 | FlowJobService |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/FlowJobService.java |
| 包名 | com.welab.wefe.board.service.service |
| 依赖项 | ['com.welab.wefe.board.service.api.project.job.QueryApi', 'com.welab.wefe.board.service.database.entity.job.JobMySqlModel', 'com.welab.wefe.board.service.database.entity.job.ProjectFlowMySqlModel', 'com.welab.wefe.board.service.database.entity.job.ProjectMySqlModel', 'com.welab.wefe.board.service.database.entity.job.TaskMySqlModel', 'com.welab.wefe.board.service.database.repository.JobRepository', 'com.welab.wefe.board.service.dto.base.PagingOutput', 'com.welab.wefe.board.service.dto.entity.job.JobListOutputModel', 'com.welab.wefe.board.service.dto.entity.job.JobOutputModel', 'com.welab.wefe.board.service.dto.vo.JobProgressOutput', 'com.welab.wefe.common.data.mysql.Where', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.web.util.ModelMapper', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'com.welab.wefe.common.wefe.enums.JobStatus', 'com.welab.wefe.common.wefe.enums.TaskStatus', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.data.jpa.domain.Specification', 'org.springframework.stereotype.Service', 'java.util.List'] |
| 概述说明 | FlowJobService提供流作业管理功能：分页查询执行历史(query)、获取作业详情(detail)和进度(getProgress)。依赖多个服务与仓库，通过条件筛选、状态判断返回对应数据模型。 |

# 说明

FlowJobService是一个服务类，继承自AbstractService，用于管理流程作业的执行记录、详情和进度查询。它依赖JobRepository、TaskService、ProjectFlowService、ProjectService和JobService等组件。主要功能包括分页查询流程执行历史记录，根据条件筛选作业；获取作业详情，支持通过流程ID或作业ID查询；以及获取作业执行进度，根据作业状态和任务状态确定当前执行节点，返回进度信息。进度查询逻辑涵盖运行中、异常中断、手动中断和未开始等多种状态处理。

# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| FlowJobService | class | FlowJobService提供流作业管理功能，包括分页查询执行记录、获取作业详情及进度。依赖多个服务处理数据，支持按条件筛选作业，根据状态返回进度信息。 |



## 类 FlowJobService

|      |      |
|------|------|
| 访问范围 | @Service;public |
| 类型 | class |
| 名称 | FlowJobService |
| 说明 | FlowJobService提供流作业管理功能，包括分页查询执行记录、获取作业详情及进度。依赖多个服务处理数据，支持按条件筛选作业，根据状态返回进度信息。 |


### UML类图

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

    FlowJobService --|> AbstractService : 继承
    FlowJobService --> JobRepository : 依赖
    FlowJobService --> TaskService : 依赖
    FlowJobService --> ProjectFlowService : 依赖
    FlowJobService --> ProjectService : 依赖
    FlowJobService --> JobService : 依赖
    FlowJobService --> QueryApi : 使用Input参数
    JobRepository --> JobMySqlModel : 操作
    TaskService --> TaskMySqlModel : 操作
    ProjectFlowService --> ProjectFlowMySqlModel : 操作
    ProjectService --> ProjectMySqlModel : 操作
    JobService --> JobMySqlModel : 操作
    QueryApi$Input --> JobListOutputModel : 映射
    JobProgressOutput --> JobMySqlModel : 包含
    JobProgressOutput --> TaskMySqlModel : 包含
```

类图描述：
FlowJobService是一个服务类，继承自AbstractService，主要处理流程作业的相关操作。它依赖多个服务类（JobRepository、TaskService等）和模型类（JobMySqlModel、TaskMySqlModel等），提供查询作业历史记录、获取作业详情和进度等功能。类图清晰地展示了这些类之间的继承、依赖和关联关系，体现了系统的分层架构设计。


### 内部方法调用关系图

```mermaid
graph TD
    A["类FlowJobService"]
    B["属性: JobRepository jobRepo"]
    C["属性: TaskService taskService"]
    D["属性: ProjectFlowService projectFlowService"]
    E["属性: ProjectService projectService"]
    F["属性: JobService jobService"]
    G["方法: query(QueryApi.Input input)"]
    H["方法: detail(String flowId, String jobId, JobMemberRole role)"]
    I["方法: getProgress(String jobId, JobMemberRole role)"]
    J["子流程: 构建Specification条件"]
    K["调用: jobRepo.paging"]
    L["条件判断: jobId是否为空"]
    M["调用: projectFlowService.findOne"]
    N["调用: projectService.findByProjectId"]
    O["调用: jobRepo.findLastByFlowId"]
    P["调用: jobRepo.findByJobId"]
    Q["调用: ModelMapper.map"]
    R["调用: jobService.findByJobId"]
    S["调用: taskService.listByJobId"]
    T["条件分支: 任务状态处理"]
    U["流处理: 筛选running/error/stop/wait_run状态任务"]
    V["返回: JobProgressOutput.success"]

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
    L --"是"--> M --> N --> O
    L --"否"--> P
    O & P --> Q
    I --> R --> S --> T
    T --"success"--> "取末项任务"
    T --"wait_run"--> "返回null"
    T --"其他状态"--> U --> V
```

流程图描述：该流程图展示了FlowJobService类的三个核心方法。query方法通过构建Specification条件进行分页查询；detail方法根据jobId是否为空分别查询最新流程任务或指定任务，最终映射为输出模型；getProgress方法通过多级状态判断（包括运行中、异常中断、手动停止等）确定任务进度，其中包含复杂的流式过滤逻辑。各方法均通过组合不同仓储和服务调用完成业务逻辑，体现了任务状态机的处理过程。

### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| projectFlowService | ProjectFlowService | 自动注入ProjectFlowService实例。 |
| jobRepo | JobRepository | 自动注入JobRepository实例到jobRepo变量。 |
| jobService | JobService | 自动注入JobService实例。 |
| projectService | ProjectService | 使用@Autowired自动注入ProjectService实例。 |
| taskService | TaskService | 使用@Autowired自动注入TaskService实例。 |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| query | PagingOutput<JobListOutputModel> | 该方法根据输入条件查询任务列表，通过流ID、任务ID、状态、非仲裁者角色和名称模糊匹配构建查询条件，返回分页结果。 |
| detail | JobOutputModel | 该方法根据流程ID和任务ID查询任务详情。若无任务ID，则查询流程的最后任务；否则按任务ID查询。返回任务详情或null。 |
| getProgress | JobProgressOutput | 获取任务进度：根据任务ID和角色查询任务状态，返回任务及当前执行节点信息。处理成功、待运行、异常中断等状态，确保结果准确。 |




