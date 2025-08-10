# Basic Information

|      |      |
|------|------|
| Name | CallbackService |
| Language | .java |
| Code Path | WeFe/fusion/fusion-service/src/main/java/com/welab/wefe/data/fusion/service/service/CallbackService.java |
| Package Name | com.welab.wefe.data.fusion.service.service |
| Dependencies | ['com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.web.util.ModelMapper', 'com.welab.wefe.data.fusion.service.actuator.rsapsi.PsiClientActuator', 'com.welab.wefe.data.fusion.service.api.thirdparty.CallbackApi', 'com.welab.wefe.data.fusion.service.database.entity.PartnerMySqlModel', 'com.welab.wefe.data.fusion.service.database.entity.TaskMySqlModel', 'com.welab.wefe.data.fusion.service.database.repository.TaskRepository', 'com.welab.wefe.data.fusion.service.dto.entity.PartnerOutputModel', 'com.welab.wefe.data.fusion.service.enums.PSIActuatorStatus', 'com.welab.wefe.data.fusion.service.enums.TaskStatus', 'com.welab.wefe.data.fusion.service.manager.ActuatorManager', 'com.welab.wefe.data.fusion.service.task.AbstractTask', 'com.welab.wefe.data.fusion.service.task.PsiClientTask', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'com.welab.wefe.data.fusion.service.task.PsiServerTask', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.stereotype.Service', 'java.net.URL', 'com.welab.wefe.common.StatusCode.DATA_NOT_FOUND'] |
| Brief Description | The CallbackService handles callback requests and performs different operations based on their types: running starts a client task, init updates the task status, success concludes the task, and stop terminates the task. It involves collaboration with TaskService, TaskRepository, and PartnerService. |

# Description

CallbackService is a service class designed to handle callback requests, with its primary functions including executing corresponding operations based on different types of callback inputs. It relies on TaskService, TaskRepository, and PartnerService for managing task and partner data. The callback types include running, init, success, and stop, each corresponding to distinct processing logic for task execution, initialization, completion, and termination. The running method initiates the client task when the partner server is ready, the init method updates the task status to pending, the success method completes the task and destroys the task instance, and the stop method terminates the server task and sets the status to abnormal. The service also includes a helper method for extracting URL domains.

# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| CallbackService | class | The CallbackService handles callback requests and performs different operations based on their types: running starts client tasks, init updates task status, success concludes tasks, and stop terminates tasks. It includes task status management and partner information processing. |



## Class CallbackService

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | CallbackService |
| Description | The CallbackService handles callback requests and performs different operations based on their types: running starts client tasks, init updates task status, success concludes tasks, and stop terminates tasks. It includes task status management and partner information processing. |


### UML Class Diagram

```mermaid
classDiagram
    class CallbackService {
        -TaskService taskService
        -TaskRepository taskRepository
        -PartnerService partnerService
        +callback(CallbackApi.Input input) void
        -running(String businessId, String ip, int port) void
        -stop(String businessId) void
        -getUrlHost(String urlStr) String
    }

    class TaskService {
        <<Interface>>
        +findByBusinessId(String businessId) TaskMySqlModel
    }

    class TaskRepository {
        <<Interface>>
        +save(TaskMySqlModel task) void
    }

    class PartnerService {
        <<Interface>>
        +findByPartnerId(String partnerId) PartnerMySqlModel
    }

    class ActuatorManager {
        <<Singleton>>
        +get(String businessId) AbstractTask
        +set(AbstractTask task) void
    }

    class AbstractTask {
        <<Abstract>>
        +finish() void
        +run() void
        +close() void
    }

    class PsiClientTask {
        +PsiClientTask(String businessId, PsiClientActuator actuator)
    }

    class PsiServerTask {
        +close() void
    }

    class CallbackApi$Input {
        +getType() Enum
        +getBusinessId() String
        +getSocketIp() String
        +getSocketPort() int
        +getDataCount() int
    }

    class TaskMySqlModel {
        +setDataCount(int count) void
        +setStatus(TaskStatus status) void
        +getPartnerMemberId() String
        +getDataResourceId() String
        +isTrace() boolean
        +getTraceColumn() String
    }

    class PartnerMySqlModel {
        +getBaseUrl() String
    }

    class PartnerOutputModel {
        // Data transfer object
    }

    CallbackService --> TaskService : depends
    CallbackService --> TaskRepository : depends
    CallbackService --> PartnerService : depends
    CallbackService --> ActuatorManager : depends
    CallbackService --> CallbackApi$Input : processes input
    AbstractTask <|-- PsiClientTask
    AbstractTask <|-- PsiServerTask
    PartnerService ..> PartnerMySqlModel : returns
    TaskService ..> TaskMySqlModel : returns
```

Class diagram description: This diagram illustrates the core structure of the CallbackService, which handles different types of callback requests by depending on TaskService, TaskRepository, and PartnerService. Key functionalities include managing task state changes such as initialization (running), success, and termination (stop), as well as controlling task executors via ActuatorManager. The system employs the abstract factory pattern, with AbstractTask serving as the base class for concrete implementations like PsiClientTask and PsiServerTask. Components collaborate through well-defined interfaces, demonstrating a clear layered design approach.


### Internal Method Call Graph

```mermaid
graph TD
    A["CallbackService Class"]
    B["Attribute: Logger LOG"]
    C["Attribute: TaskService taskService"]
    D["Attribute: TaskRepository taskRepository"]
    E["Attribute: PartnerService partnerService"]
    F["Method: callback(CallbackApi.Input input)"]
    G["Method: running(String businessId, String ip, int port)"]
    H["Method: stop(String businessId)"]
    I["Method: getUrlHost(String urlStr)"]
    J["switch(input.getType())"]
    K["case 'running'"]
    L["case 'init'"]
    M["case 'success'"]
    N["case 'stop'"]
    O["default exception handling"]
    P["taskService.findByBusinessId"]
    Q["taskRepository.save"]
    R["ActuatorManager.get"]
    S["AbstractTask.finish"]
    T["PsiClientTask initialization"]
    U["ActuatorManager.set"]
    V["AbstractTask.run"]
    W["partnerService.findByPartnerId"]
    X["ModelMapper.map"]
    Y["URL parsing"]

    A --> B
    A --> C
    A --> D
    A --> E
    A --> F
    F --> J
    J --> K --> G
    J --> L --> P --> Q
    J --> M --> R --> S
    J --> N --> H
    J --> O
    G --> R
    G --> P
    G --> W
    G --> Y
    G --> Q
    G --> T --> U --> V
    H --> R
    H --> PsiServerTask operation
    A --> I --> Y
```

This flowchart illustrates the complete processing logic of the CallbackService class, primarily showing the branch handling flow of the callback method based on different types (running/init/success/stop). The running branch initiates client tasks, the init branch updates task status, the success branch terminates tasks, and the stop branch shuts down server tasks. The core process involves component interactions such as task querying, status updates, actuator management, and partner information processing. Clear arrow connections demonstrate the complete business processing chain and exception handling path.

### Field List

| Name  | Type  | Description |
|-------|-------|------|
| partnerService | PartnerService | Use @Autowired to automatically inject an instance of PartnerService. |
| taskRepository | TaskRepository | Use @Autowired to automatically inject an instance of TaskRepository. |
| taskService | TaskService | Automatically inject the TaskService instance. |
| LOG = LoggerFactory.getLogger(CallbackService.class) | Logger | A protected static logger instance is defined in the CallbackService class. |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| running | void | The method `running` checks the task status, creates and starts a PsiClientTask after updating it to Running. It reports an error or logs if the task or collaborator does not exist. |
| stop | void | This method retrieves the PSI service task by businessId, sets the executor status to abnormal and terminates the task, throwing a system error exception when an error occurs. |
| getUrlHost | String | The method resolves the input string through the URL class to obtain the hostname, logs an exception if it occurs, and returns null. |
| callback | void | The method handles different tasks based on the input type: calls `running` during execution, updates the task status to pending during initialization, ends the task upon success, calls `stop` when stopping, and throws an exception in other cases. |




