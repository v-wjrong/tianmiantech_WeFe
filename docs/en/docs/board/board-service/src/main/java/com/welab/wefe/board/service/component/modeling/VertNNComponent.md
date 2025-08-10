# Basic Information

|      |      |
|------|------|
| Name | VertNNComponent |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/component/modeling/VertNNComponent.java |
| Package Name | com.welab.wefe.board.service.component.modeling |
| Dependencies | ['com.alibaba.fastjson.JSONObject', 'com.welab.wefe.board.service.component.base.io.IODataType', 'com.welab.wefe.board.service.component.base.io.InputMatcher', 'com.welab.wefe.board.service.component.base.io.Names', 'com.welab.wefe.board.service.component.base.io.OutputItem', 'com.welab.wefe.board.service.database.entity.job.JobMemberMySqlModel', 'com.welab.wefe.board.service.database.entity.job.TaskMySqlModel', 'com.welab.wefe.board.service.database.entity.job.TaskResultMySqlModel', 'com.welab.wefe.board.service.exception.FlowNodeException', 'com.welab.wefe.board.service.model.FlowGraph', 'com.welab.wefe.board.service.model.FlowGraphNode', 'com.welab.wefe.board.service.model.JobBuilder', 'com.welab.wefe.common.fieldvalidate.AbstractCheckModel', 'com.welab.wefe.common.fieldvalidate.annotation.Check', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.wefe.enums.ComponentType', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'org.springframework.stereotype.Service', 'java.util.ArrayList', 'java.util.Arrays', 'java.util.List'] |
| Brief Description | VertNNComponent is a vertical deep learning component that checks the number of collaborating parties and generates task parameters, including training parameters, neural network structure definitions, and input-output configurations. |

# Description

VertNNComponent is a vertical deep learning component that inherits from AbstractModelingComponent and is used to construct deep learning tasks. Before building a task, it checks the number of collaborating parties to ensure it does not exceed one. The component generates task parameters through the createTaskParams method, including configurations such as training epochs, learning rate, batch size, optimizer, loss function, etc., and defines the neural network structures for the bottom, interactive, and top layers. Inputs include training and evaluation datasets, while outputs consist of dataset instances and trained models. The Params class contains all necessary training parameters and network layer definitions, with each layer including the class name and configuration parameters such as dimensions, activation functions, etc.

# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| VertNNComponent | class | VertNNComponent is a vertical deep learning component that verifies the number of collaborating parties and generates task parameters, including model architecture, optimizer, and training configuration. |



## Class VertNNComponent

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | VertNNComponent |
| Description | VertNNComponent is a vertical deep learning component that verifies the number of collaborating parties and generates task parameters, including model architecture, optimizer, and training configuration. |


### UML Class Diagram

```mermaid
classDiagram
    class VertNNComponent {
        +VertNNComponent()
        +checkBeforeBuildTask(FlowGraph graph, List~TaskMySqlModel~ preTasks, FlowGraphNode node, Params params) void
        +createTaskParams(JobBuilder jobBuilder, FlowGraph graph, List~TaskMySqlModel~ preTasks, FlowGraphNode node, Params params) JSONObject
        +taskType() ComponentType
        +getAllResult(String taskId) List~TaskResultMySqlModel~
        +getResult(String taskId, String type) TaskResultMySqlModel
        +inputs(FlowGraph graph, FlowGraphNode node) List~InputMatcher~
        +outputs(FlowGraph graph, FlowGraphNode node) List~OutputItem~
    }

    class AbstractModelingComponent~T~ {
        <<Abstract>>
        +AbstractModelingComponent()
        #checkBeforeBuildTask(FlowGraph graph, List~TaskMySqlModel~ preTasks, FlowGraphNode node, T params) void
        #createTaskParams(JobBuilder jobBuilder, FlowGraph graph, List~TaskMySqlModel~ preTasks, FlowGraphNode node, T params) JSONObject
        +taskType() ComponentType
        #getAllResult(String taskId) List~TaskResultMySqlModel~
        #getResult(String taskId, String type) TaskResultMySqlModel
        #inputs(FlowGraph graph, FlowGraphNode node) List~InputMatcher~
        +outputs(FlowGraph graph, FlowGraphNode node) List~OutputItem~
    }

    class Params {
        -int epochs
        -float interactiveLayerLr
        -int batchSize
        -float learningRate
        -String optimizer
        -String loss
        -BottomNNDefine bottomNNDefine
        -InteractiveLayerDefine interactiveLayerDefine
        -TopNNDefine topNNDefine
        +getEpochs() int
        +setEpochs(int epochs) void
        // ...Other getters/setters omitted...
    }

    class BottomNNDefine {
        -List~Layer~ layers
        +getLayers() List~Layer~
        +setLayers(List~Layer~ layers) void
    }

    class InteractiveLayerDefine {
        -List~Layer~ layers
        +getLayers() List~Layer~
        +setLayers(List~Layer~ layers) void
    }

    class TopNNDefine {
        -List~Layer~ layers
        +getLayers() List~Layer~
        +setLayers(List~Layer~ layers) void
    }

    class Layer {
        -String className
        -LayerConfig config
        +getClassName() String
        +setClassName(String className) void
        +getConfig() LayerConfig
        +setConfig(LayerConfig config) void
    }

    class LayerConfig {
        -int units
        -List~Integer~ inputShape
        -String activation
        +getUnits() int
        +setUnits(int units) void
        // ...Other getters/setters omitted...
    }

    VertNNComponent --|> AbstractModelingComponent~Params~ : Inheritance
    Params --* BottomNNDefine : Composition
    Params --* InteractiveLayerDefine : Composition
    Params --* TopNNDefine : Composition
    BottomNNDefine --* Layer : Composition
    InteractiveLayerDefine --* Layer : Composition
    TopNNDefine --* Layer : Composition
    Layer --* LayerConfig : Composition
```

Class diagram description: This diagram illustrates the inheritance relationship where the VertNNComponent class extends the generic class AbstractModelingComponent~Params~. The Params class internally contains multiple neural network definition classes (BottomNNDefine, InteractiveLayerDefine, TopNNDefine), which in turn contain Layer objects. Layers further encapsulate LayerConfig configuration items. The overall structure presents the parameter system and hierarchical relationships of a vertical deep learning component, demonstrating its capability for parameterized configuration of neural network architectures.


### Internal Method Call Graph

```mermaid
graph TD
    A["Class VertNNComponent"]
    B["Method: checkBeforeBuildTask"]
    C["Method: createTaskParams"]
    D["Method: taskType"]
    E["Method: getAllResult"]
    F["Method: getResult"]
    G["Method: inputs"]
    H["Method: outputs"]
    I["Inner Class Params"]
    J["Properties: epochs/interactiveLayerLr/batchSize etc."]
    K["Inner Class BottomNNDefine"]
    L["Inner Class InteractiveLayerDefine"]
    M["Inner Class TopNNDefine"]
    N["Inner Class Layer"]
    O["Inner Class LayerConfig"]

    A --> B
    A --> C
    A --> D
    A --> E
    A --> F
    A --> G
    A --> H
    A --> I
    I --> J
    I --> K
    I --> L
    I --> M
    K --> N
    L --> N
    M --> N
    N --> O
```

```mermaid
sequenceDiagram
    participant A as VertNNComponent
    participant B as FlowGraph
    participant C as JobBuilder
    participant D as JObject

    A->>B: checkBeforeBuildTask(graph, preTasks, node, params)
    B-->>A: jobMembers
    A->>B: getMembers()
    A->>A: validate providerCount
    A->>C: createTaskParams(jobBuilder, graph, preTasks, node, params)
    C->>D: create vertNNParam
    D->>D: append parameters(epochs/batchSize etc.)
    D->>D: append optimizer config
    D->>D: append neural network structure(bottom/interactive/top)
    D-->>A: return vertNNParam
```

This flowchart demonstrates the core structure of the VertNNComponent class and its key method invocation relationships. As a vertical deep learning component, it validates input data compliance through checkBeforeBuildTask, and constructs a JSON object containing neural network architecture and optimizer parameters via createTaskParams. The inner Params class and its nested classes define a comprehensive neural network parameter system, including layer configurations and optimization strategies essential for deep learning. The sequence diagram highlights the parameter validation and configuration generation process during task creation.

### Field List

| Name  | Type  | Description |
|-------|-------|------|

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getAllResult | List<TaskResultMySqlModel> | This is a Java method that overrides the getAllResult method of the parent class, retrieving a list of all task results for a specified taskId through the listAllResult method of taskResultService. |
| taskType | ComponentType | Method override, returns component type as VertNN. |
| createTaskParams | JSONObject | Method to create a task parameter JSON object, including training parameters such as epochs, batch_size, optimizer settings, loss function, evaluation metrics, as well as neural network structure definitions (bottom, interactive, top layers), with configuration type set to keras. |
| checkBeforeBuildTask | void | Verify the number of collaborating parties before checking the build task, and if it exceeds 1, report an error indicating that only a single collaborating party is supported. |
| getResult | TaskResultMySqlModel | Override the parent class method to retrieve MySQL model results based on task ID and type. |
| inputs | List<InputMatcher> | Method override, returns two input matchers: the training dataset and the evaluation dataset, corresponding to the filter and the provider respectively. |
| outputs | List<OutputItem> | Method override, returns a list of output items containing dataset instances and neural network models. |




