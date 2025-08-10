# Basic Information

|      |      |
|------|------|
| Name | TaskOutputView |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/dto/entity/job/TaskOutputView.java |
| Package Name | com.welab.wefe.board.service.dto.entity.job |
| Dependencies | ['com.welab.wefe.board.service.database.entity.job.TaskMySqlModel', 'com.welab.wefe.board.service.dto.entity.AbstractOutputModel', 'com.welab.wefe.common.fieldvalidate.annotation.Check', 'com.welab.wefe.common.web.util.ModelMapper', 'java.util.List'] |
| Brief Description | The TaskOutputView class inherits from AbstractOutputModel, containing a TaskOutputModel task and a list of TaskResultOutputModel results, providing constructor methods and getter/setter. |

# Description

The TaskOutputView class inherits from AbstractOutputModel and contains two main fields: task and results. The task field is annotated as the task created by the component, with the type TaskOutputModel; the results field is annotated as the output results of the task, with the type being a list of TaskResultOutputModel. The class provides three constructors: a default constructor, a constructor that accepts a TaskMySqlModel parameter, and a constructor that accepts a TaskMySqlModel and a list of TaskResultOutputModel parameters. The latter uses ModelMapper to map TaskMySqlModel to TaskOutputModel. The class also provides getter and setter methods for the task and results fields.

# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| TaskOutputView | class | The TaskOutputView class inherits from AbstractOutputModel and contains task and results attributes, providing constructors and getter/setter methods. The task is mapped from TaskMySqlModel, while results is a list of TaskResultOutputModel. |



## Class TaskOutputView

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | TaskOutputView |
| Description | The TaskOutputView class inherits from AbstractOutputModel and contains task and results attributes, providing constructors and getter/setter methods. The task is mapped from TaskMySqlModel, while results is a list of TaskResultOutputModel. |


### UML Class Diagram

```mermaid
classDiagram
    class AbstractOutputModel {
        <<Abstract>>
    }
    
    class TaskOutputView {
        -TaskOutputModel task
        -List~TaskResultOutputModel~ results
        +TaskOutputView()
        +TaskOutputView(TaskMySqlModel task)
        +TaskOutputView(TaskMySqlModel task, List~TaskResultOutputModel~ results)
        +TaskOutputModel getTask()
        +void setTask(TaskOutputModel task)
        +List~TaskResultOutputModel~ getResults()
        +void setResults(List~TaskResultOutputModel~ results)
    }
    
    class TaskOutputModel {
    }
    
    class TaskResultOutputModel {
    }
    
    class TaskMySqlModel {
    }
    
    class ModelMapper {
        +~T~ map(Object source, Class~T~ targetClass)
    }
    
    AbstractOutputModel <|-- TaskOutputView
    TaskOutputView --> TaskOutputModel : contains
    TaskOutputView --> TaskResultOutputModel : aggregates
    TaskOutputView --> TaskMySqlModel : conversion dependency
    TaskOutputView ..> ModelMapper : invokes
```

Class diagram description: TaskOutputView inherits from the abstract class AbstractOutputModel and contains private members TaskOutputModel and a list of TaskResultOutputModel. It converts data from TaskMySqlModel through constructors and relies on ModelMapper for object mapping. This class provides standard getter/setter methods, maintains associations with multiple model classes, and implements the encapsulation and conversion functionality for task output data.


### Internal Method Call Graph

```mermaid
graph TD
    A["Class TaskOutputView"]
    B["Inherits from: AbstractOutputModel"]
    C["Annotation property: @Check TaskOutputModel task"]
    D["Annotation property: @Check List<TaskResultOutputModel> results"]
    E["Constructor: TaskOutputView()"]
    F["Constructor: TaskOutputView(TaskMySqlModel task)"]
    G["Constructor: TaskOutputView(TaskMySqlModel task, List<TaskResultOutputModel> results)"]
    H["Method: getTask()/setTask()"]
    I["Method: getResults()/setResults()"]
    J["Internal operation: ModelMapper.map()"]

    A --> B
    A --> C
    A --> D
    A --> E
    A --> F
    A --> G
    A --> H
    A --> I
    G --> J
```

This flowchart illustrates the complete structure of the TaskOutputView class, including inheritance relationships, annotation properties, three overloaded constructors, and getter/setter methods. The core construction process utilizes ModelMapper for model conversion, mapping TaskMySqlModel to TaskOutputModel. The class design adheres to data encapsulation principles, employs annotations for validation markers, and supports flexible result set injection approaches.

### Field List

| Name  | Type  | Description |
|-------|-------|------|
| task | TaskOutputModel | Component-created task output model |
| results | List<TaskResultOutputModel> | The class member variable `results`, of type `TaskResultOutputModel` list, is annotated with `@Check` and labeled as "task output results". |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| setResults | void | Methods for setting up task result lists. |
| getTask | TaskOutputModel | The method getTask returns a task object of type TaskOutputModel. |
| getResults | List<TaskResultOutputModel> | The method to obtain the task result list returns a collection of type TaskResultOutputModel. |
| setTask | void | Set the task object. |




