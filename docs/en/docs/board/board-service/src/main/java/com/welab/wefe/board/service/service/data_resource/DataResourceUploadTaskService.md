# Basic Information

|      |      |
|------|------|
| Name | DataResourceUploadTaskService |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/data_resource/DataResourceUploadTaskService.java |
| Package Name | com.welab.wefe.board.service.service.data_resource |
| Dependencies | ['com.welab.wefe.board.service.api.data_resource.upload_task.DataResourceUploadTaskQueryApi', 'com.welab.wefe.board.service.database.entity.data_resource.DataResourceMysqlModel', 'com.welab.wefe.board.service.database.entity.data_resource.DataResourceUploadTaskMysqlModel', 'com.welab.wefe.board.service.database.repository.data_resource.DataResourceRepository', 'com.welab.wefe.board.service.database.repository.data_resource.DataResourceUploadTaskRepository', 'com.welab.wefe.board.service.dto.base.PagingOutput', 'com.welab.wefe.board.service.dto.entity.data_resource.output.DataResourceUploadTaskOutputModel', 'com.welab.wefe.board.service.dto.vo.data_resource.AbstractDataResourceUpdateInputModel', 'com.welab.wefe.board.service.service.AbstractService', 'com.welab.wefe.common.Convert', 'com.welab.wefe.common.TimeSpan', 'com.welab.wefe.common.data.mysql.Where', 'com.welab.wefe.common.util.DateUtil', 'com.welab.wefe.common.wefe.enums.DataResourceType', 'com.welab.wefe.common.wefe.enums.DataResourceUploadStatus', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.data.jpa.domain.Specification', 'org.springframework.stereotype.Service', 'java.util.Date', 'java.util.function.Consumer'] |
| Brief Description | The DataResourceUploadTaskService manages data resource upload tasks, including creation, progress updates, completion, and error handling. It employs locks to ensure concurrency safety and supports querying and state management. |

# Description

The DataResourceUploadTaskService is a service class designed for managing data resource upload tasks, inheriting from AbstractService. It interacts with the database through DataResourceUploadTaskRepository and DataResourceRepository, providing functionalities such as task creation, progress updates, completion handling, and error management. Key operations include: cleaning up historical data and timed-out tasks when creating new tasks; employing synchronization locks to ensure concurrent operation safety; calculating and updating upload progress, including data row counts, completion percentages, and estimated remaining time; marking tasks as completed or failed; and supporting task queries by ID or resource ID. The service also includes pagination capabilities for retrieving lists of recently updated tasks.

# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| DataResourceUploadTaskService | class | The DataResourceUploadTaskService handles data resource upload tasks, including task creation, progress updates, completion, and error handling, using locks to ensure concurrency safety. |



## Class DataResourceUploadTaskService

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | DataResourceUploadTaskService |
| Description | The DataResourceUploadTaskService handles data resource upload tasks, including task creation, progress updates, completion, and error handling, using locks to ensure concurrency safety. |


### UML Class Diagram

```mermaid
classDiagram
    class AbstractService {
        <<Abstract>>
    }

    class DataResourceUploadTaskService {
        -Object LOCKER
        -DataResourceRepository dataResourceRepository
        -DataResourceUploadTaskRepository dataResourceUploadTaskRepository
        +newTask(DataResourceType dataResourceType, AbstractDataResourceUpdateInputModel input) DataResourceUploadTaskMysqlModel
        +findByDataResourceId(String dataResource) DataResourceUploadTaskMysqlModel
        +updateMessageBeforeStart(String dataResourceId, String message) void
        +updateProgress(String dataResourceId, long totalDataRowCount, long completedDataCount, long invalidDataCount) void
        +updateProgress(String dataResourceId, long totalDataRowCount, long completedDataCount, long invalidDataCount, String message) void
        +complete(String dataResourceId) void
        +findById(String id) DataResourceUploadTaskMysqlModel
        +update(DataResourceUploadTaskMysqlModel dataSetTask, Consumer~DataResourceUploadTaskMysqlModel~ func) void
        +query(DataResourceUploadTaskQueryApi$Input input) PagingOutput~DataResourceUploadTaskOutputModel~
        +onError(String dataResourceId, Exception e) void
    }

    class DataResourceUploadTaskMysqlModel {
        -String dataResourceName
        -int progressRatio
        -String dataResourceId
        -DataResourceUploadStatus status
        -DataResourceType dataResourceType
        -long totalDataCount
        -long invalidDataCount
        -long completedDataCount
        -long estimateRemainingTime
        -String errorMessage
        -Date createdTime
        -Date updatedTime
        +setters/getters...
    }

    class DataResourceRepository {
        <<Interface>>
    }

    class DataResourceUploadTaskRepository {
        <<Interface>>
        +deleteHistory() void
        +closeTimeoutTask() void
        +save(DataResourceUploadTaskMysqlModel task) void
        +findOne(Specification~DataResourceUploadTaskMysqlModel~ where) Optional~DataResourceUploadTaskMysqlModel~
        +findById(String id) Optional~DataResourceUploadTaskMysqlModel~
        +paging(Specification~DataResourceUploadTaskMysqlModel~ where, DataResourceUploadTaskQueryApi$Input input, Class~DataResourceUploadTaskOutputModel~ clazz) PagingOutput~DataResourceUploadTaskOutputModel~
    }

    AbstractService <|-- DataResourceUploadTaskService
    DataResourceUploadTaskService --> DataResourceRepository : Dependency
    DataResourceUploadTaskService --> DataResourceUploadTaskRepository : Dependency
    DataResourceUploadTaskRepository ..> DataResourceUploadTaskMysqlModel : Operates
```

This code demonstrates a data resource upload task service `DataResourceUploadTaskService`, which inherits from `AbstractService` and depends on two repository interfaces: `DataResourceRepository` and `DataResourceUploadTaskRepository`. Its primary functionalities include creating upload tasks, querying tasks, updating progress, completing tasks, and handling errors. It ensures thread-safe concurrent operations through a synchronization lock mechanism, using `DataResourceUploadTaskMysqlModel` as the task entity model with fields such as task status, progress, and error messages. The service provides comprehensive task lifecycle management features, including progress calculation, time estimation, and state transitions.


### Internal Method Call Graph

```mermaid
graph TD
    A["Class DataResourceUploadTaskService"]
    B["Property: Object LOCKER"]
    C["Property: DataResourceRepository dataResourceRepository"]
    D["Property: DataResourceUploadTaskRepository dataResourceUploadTaskRepository"]
    E["Method: newTask(DataResourceType, AbstractDataResourceUpdateInputModel)"]
    F["Method: findByDataResourceId(String)"]
    G["Method: updateMessageBeforeStart(String, String)"]
    H["Method: updateProgress(String, long, long, long)"]
    I["Method: updateProgress(String, long, long, long, String)"]
    J["Method: complete(String)"]
    K["Method: findById(String)"]
    L["Method: update(DataResourceUploadTaskMysqlModel, Consumer)"]
    M["Method: query(DataResourceUploadTaskQueryApi.Input)"]
    N["Method: onError(String, Exception)"]

    A --> B
    A --> C
    A --> D
    A --> E
    A --> F
    A --> G
    A --> H
    A --> I
    A --> J
    A --> K
    A --> L
    A --> M
    A --> N

    E --> F
    G --> I
    H --> I
    I --> F
    I --> J
    J --> F
    N --> F
```

```mermaid
sequenceDiagram
    participant Client
    participant Service as DataResourceUploadTaskService
    participant Repository as DataResourceUploadTaskRepository

    Client->>Service: newTask(dataResourceType, input)
    Service->>Repository: deleteHistory()
    Service->>Repository: closeTimeoutTask()
    Service->>Service: Create new task model
    Service->>Repository: save(task)
    Service-->>Client: Return task model

    Client->>Service: updateProgress(dataResourceId, totalDataRowCount, completedDataCount, invalidDataCount, message)
    Service->>Service: synchronized (LOCKER)
    Service->>Service: findByDataResourceId(dataResourceId)
    Service->>Service: Calculate progress and ETA
    Service->>Repository: save(task)
    Service-->>Client: No return value

    Client->>Service: complete(dataResourceId)
    Service->>Service: synchronized (LOCKER)
    Service->>Service: findByDataResourceId(dataResourceId)
    Service->>Repository: save(task)
    Service-->>Client: No return value

    Client->>Service: onError(dataResourceId, e)
    Service->>Service: synchronized (LOCKER)
    Service->>Service: findByDataResourceId(dataResourceId)
    Service->>Repository: save(task)
    Service-->>Client: No return value
```

This code implements a data resource upload task service with core functionalities including creating new tasks, updating task progress, marking task completion, and error handling. The flowchart illustrates the class structure and internal method invocation relationships, while the sequence diagram details the execution flow of key methods. All operations involving task state changes are thread-safe through synchronized blocks and retrieve task entities via the unified findByDataResourceId method. The progress update logic incorporates various edge case handling such as division-by-zero prevention and progress value enforcement.

### Field List

| Name  | Type  | Description |
|-------|-------|------|
| dataResourceUploadTaskRepository | DataResourceUploadTaskRepository | Automatically inject data resource upload task repository instance. |
| LOCKER = new Object() | Object | Define a static immutable object LOCKER as a synchronization lock. |
| dataResourceRepository | DataResourceRepository | Automatically inject the DataResourceRepository instance. |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| complete | void | The method `complete` synchronously updates the data resource upload task status to "completed," setting the completion count, remaining time, progress ratio, update time, and error information, then saves them. |
| updateProgress | void | Synchronously update the progress of data resource upload tasks, including calculating the progress ratio and estimating the remaining time, while ensuring thread safety and progress rationality. |
| updateMessageBeforeStart | void | Update the progress information before starting the data resource, setting the initial progress to 0 with an accompanying message. |
| findByDataResourceId | DataResourceUploadTaskMysqlModel | This method queries the database for upload task records using the data resource ID, employing a conditional constructor to specify the query criteria, and returns matching records or null. |
| newTask | DataResourceUploadTaskMysqlModel | Create a new upload task, delete old data and close timed-out tasks, then save and return after setting task attributes. |
| updateProgress | void | Update progress method, which receives the data resource ID, total number of rows, completed count, and invalid count, then calls the overloaded method for processing. |
| findById | DataResourceUploadTaskMysqlModel | This method queries the data resource upload task by ID and returns the corresponding entity or null. |
| update | void | Update dataset task: Execute callback after checking non-empty, set update time and save. |
| query | PagingOutput<DataResourceUploadTaskOutputModel> | Query data resource upload tasks, filter records with update times within the last 10 minutes, and return paginated results. |
| onError | void | The method `onError` handles data resource upload errors, synchronously updates the database task status to "failed," and records the error message and timestamp. |




