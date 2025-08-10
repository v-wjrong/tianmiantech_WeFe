# Basic Information

|      |      |
|------|------|
| Name | HorzNNComponent |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/component/modeling/HorzNNComponent.java |
| Package Name | com.welab.wefe.board.service.component.modeling |
| Dependencies | ['com.alibaba.fastjson.JSONObject', 'com.welab.wefe.board.service.component.base.io.IODataType', 'com.welab.wefe.board.service.component.base.io.InputMatcher', 'com.welab.wefe.board.service.component.base.io.Names', 'com.welab.wefe.board.service.component.base.io.OutputItem', 'com.welab.wefe.board.service.database.entity.job.TaskMySqlModel', 'com.welab.wefe.board.service.database.entity.job.TaskResultMySqlModel', 'com.welab.wefe.board.service.exception.FlowNodeException', 'com.welab.wefe.board.service.model.FlowGraph', 'com.welab.wefe.board.service.model.FlowGraphNode', 'com.welab.wefe.board.service.model.JobBuilder', 'com.welab.wefe.common.fieldvalidate.AbstractCheckModel', 'com.welab.wefe.common.fieldvalidate.annotation.Check', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.wefe.enums.ComponentType', 'org.springframework.stereotype.Service', 'java.util.ArrayList', 'java.util.Arrays', 'java.util.List'] |
| Brief Description | HorzNNComponent is a horizontal neural network component that inherits from AbstractModelingComponent, encompassing parameter validation, task creation, input/output definition, and neural network layer configuration. |

# Description

The HorzNNComponent is a Spring service class that inherits from AbstractModelingComponent, designed to implement horizontal neural network modeling tasks. This class defines model parameters through the Params inner class, including maximum iterations, batch size, learning rate, optimizer, loss function, and neural network layer definitions. The createTaskParams method constructs a JSON object containing training parameters, such as encoded labels, iteration configuration, optimizer settings, evaluation metrics, and neural network architecture definitions. The inputs and outputs methods respectively define the required input data (training set and evaluation set) and output results (dataset and trained model) for the component. The component type is HorzNN and supports fetching task results. Neural network layer definitions include class names and configuration parameters, such as dimensions, input shapes, and activation functions.

# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| HorzNNComponent | class | HorzNNComponent is a horizontal neural network component that inherits from AbstractModelingComponent, handling task parameter generation and input-output matching. It includes parameters such as maximum iterations, batch size, and learning rate, supports Keras configuration, and outputs datasets and models. |



## Class HorzNNComponent

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | HorzNNComponent |
| Description | HorzNNComponent is a horizontal neural network component that inherits from AbstractModelingComponent, handling task parameter generation and input-output matching. It includes parameters such as maximum iterations, batch size, and learning rate, supports Keras configuration, and outputs datasets and models. |


### UML Class Diagram

```mermaid
classDiagram
    class AbstractModelingComponent~T~ {
        <<Abstract>>
        +checkBeforeBuildTask(FlowGraph graph, List~TaskMySqlModel~ preTasks, FlowGraphNode node, T params) void
        +createTaskParams(JobBuilder jobBuilder, FlowGraph graph, List~TaskMySqlModel~ preTasks, FlowGraphNode node, T params) JSONObject
        +taskType() ComponentType
        +getAllResult(String taskId) List~TaskResultMySqlModel~
        +getResult(String taskId, String type) TaskResultMySqlModel
        +inputs(FlowGraph graph, FlowGraphNode node) List~InputMatcher~
        +outputs(FlowGraph graph, FlowGraphNode node) List~OutputItem~
    }

    class HorzNNComponent {
        +checkBeforeBuildTask(FlowGraph graph, List~TaskMySqlModel~ preTasks, FlowGraphNode node, Params params) void
        +createTaskParams(JobBuilder jobBuilder, FlowGraph graph, List~TaskMySqlModel~ preTasks, FlowGraphNode node, Params params) JSONObject
        +taskType() ComponentType
        +getAllResult(String taskId) List~TaskResultMySqlModel~
        +getResult(String taskId, String type) TaskResultMySqlModel
        +inputs(FlowGraph graph, FlowGraphNode node) List~InputMatcher~
        +outputs(FlowGraph graph, FlowGraphNode node) List~OutputItem~
    }

    class Params {
        -int maxIter
        -int batchSize
        -float learningRate
        -String optimizer
        -String loss
        -NNDefine nnDefine
        +getMaxIter() int
        +setMaxIter(int maxIter) void
        +getBatchSize() int
        +setBatchSize(int batchSize) void
        +getLearningRate() float
        +setLearningRate(float learningRate) void
        +getOptimizer() String
        +setOptimizer(String optimizer) void
        +getLoss() String
        +setLoss(String loss) void
        +getNnDefine() NNDefine
        +setNnDefine(NNDefine nnDefine) void
    }

    class NNDefine {
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
        +getInputShape() List~Integer~
        +setInputShape(List~Integer~ inputShape) void
        +getActivation() String
        +setActivation(String activation) void
    }

    HorzNNComponent --|> AbstractModelingComponent~Params~ : Inheritance
    Params "1" *-- "1" NNDefine : Composition
    NNDefine "1" *-- "n" Layer : Composition
    Layer "1" *-- "1" LayerConfig : Composition
```

This code describes a horizontal neural network component `HorzNNComponent`, which inherits from the generic abstract class `AbstractModelingComponent` and implements several key methods for task parameter construction, input-output matching, etc. The inner class `Params` defines hyperparameters required for neural network training (such as iteration count, batch size, etc.), and through nested classes `NNDefine`, `Layer`, and `LayerConfig`, it achieves structured definition of neural network layers. The overall design follows a layered pattern, with parameter validation implemented via `@Check` annotations, reflecting a configurable deep learning component implementation.


### Internal Method Call Graph

```mermaid
graph TD
    A["Class HorzNNComponent"]
    B["Method: checkBeforeBuildTask"]
    C["Method: createTaskParams"]
    D["Method: taskType"]
    E["Method: getAllResult"]
    F["Method: getResult"]
    G["Method: inputs"]
    H["Method: outputs"]
    I["Inner Class Params"]
    J["Properties: maxIter/batchSize/learningRate etc."]
    K["Method: getter/setter"]
    L["Inner Class NNDefine"]
    M["Properties: layers"]
    N["Inner Class Layer"]
    O["Properties: className/config"]
    P["Inner Class LayerConfig"]
    Q["Properties: units/inputShape/activation"]

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
    L --> M
    I --> N
    N --> O
    I --> P
    P --> Q
```

```mermaid
sequenceDiagram
    participant A as createTaskParams Caller
    participant B as HorzNNComponent
    participant C as JObject
    participant D as Params

    A->>B: Invoke createTaskParams(jobBuilder, graph, preTasks, node, params)
    B->>C: Create horzNNParam object
    B->>D: Retrieve maxIter/batchSize etc.
    C->>C: Append basic params (encode_label/max_iter etc.)
    B->>C: Create and append earlyStop object
    B->>C: Create and append optimizer object
    B->>C: Append metrics array
    B->>D: Retrieve nnDefine.layers
    B->>C: Create and append nnDefine object
    B->>A: Return horzNNParam
```

This flowchart presents the complete structure of the HorzNNComponent class, including 7 main methods and 4 levels of nested parameter classes. The sequence diagram details the execution process of the createTaskParams method, which constructs a JSON structure containing neural network training parameters via JObject. The structure includes basic parameters, early_stop configuration, optimizer settings, evaluation metrics, and neural network layer definitions, ultimately returning a complete parameter object. Parameters are retrieved layer by layer through the Params class and its nested classes NNDefine/Layer/LayerConfig.

### Field List

| Name  | Type  | Description |
|-------|-------|------|

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| createTaskParams | JSONObject | The method creates horizontal neural network task parameters, including the number of iterations, batch size, early stopping conditions, optimizer settings, loss function, evaluation metrics, and neural network definition. Returns a JSON-formatted parameter object. |
| getResult | TaskResultMySqlModel | Rewrite the method getResult to invoke the parent class method for obtaining the task result. |
| getAllResult | List<TaskResultMySqlModel> | This method overrides the parent class method and retrieves a list of all task results for the specified taskId by invoking the listAllResult method of taskResultService. |
| checkBeforeBuildTask | void | This is a Java method override used for pre-build task validation, with parameters including the flow chart, predecessor task list, node, and parameters, which may throw a process node exception. |
| taskType | ComponentType | Method override, returns component type as horizontal neural network. |
| inputs | List<InputMatcher> | The code overrides the parent class method, returning two InputMatcher objects that match the training dataset and the evaluation dataset, respectively. |
| outputs | List<OutputItem> | The method outputs returns two OutputItem objects, containing the dataset and model output items, and may throw a FlowNodeException. |




