# Basic Information

|      |      |
|------|------|
| Name | FeatureSelectionComponent |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/component/feature/FeatureSelectionComponent.java |
| Package Name | com.welab.wefe.board.service.component.feature |
| Dependencies | ['com.alibaba.fastjson.JSONObject', 'com.welab.wefe.board.service.component.DataIOComponent', 'com.welab.wefe.board.service.component.base.AbstractComponent', 'com.welab.wefe.board.service.component.base.io.IODataType', 'com.welab.wefe.board.service.component.base.io.InputMatcher', 'com.welab.wefe.board.service.component.base.io.Names', 'com.welab.wefe.board.service.component.base.io.OutputItem', 'com.welab.wefe.board.service.database.entity.job.TaskMySqlModel', 'com.welab.wefe.board.service.database.entity.job.TaskResultMySqlModel', 'com.welab.wefe.board.service.dto.entity.MemberFeatureInfoModel', 'com.welab.wefe.board.service.exception.FlowNodeException', 'com.welab.wefe.board.service.model.FlowGraph', 'com.welab.wefe.board.service.model.FlowGraphNode', 'com.welab.wefe.board.service.model.JobBuilder', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.fieldvalidate.AbstractCheckModel', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.wefe.enums.ComponentType', 'com.welab.wefe.common.wefe.enums.FederatedLearningType', 'org.apache.commons.collections4.CollectionUtils', 'org.springframework.stereotype.Service', 'java.util.ArrayList', 'java.util.Arrays', 'java.util.List', 'java.util.concurrent.atomic.AtomicInteger', 'java.util.stream.Collectors'] |
| Brief Description | The FeatureSelectionComponent is a feature selection component that checks whether member features are consistent, ensures the feature lists for horizontal modeling are identical, and stops task creation if no features are present. |

# Description

The FeatureSelectionComponent is a component designed for feature selection, inheriting from AbstractComponent. Its primary functions include: stopping task creation when no features are selected; checking predecessor node data to ensure participation of all members; validating feature list consistency during horizontal modeling; reorganizing frontend parameters to generate task parameters; and defining input and output data types. This component supports feature selection and includes a parameter class, Params, for members and feature lists.

# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| FeatureSelectionComponent | class | The FeatureSelectionComponent is used for feature selection, verifying the validity of members and features. Horizontal modeling requires consistent features, generating task parameters and handling input/output. The task will be terminated if there are no features or if member matching fails. |



## Class FeatureSelectionComponent

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | FeatureSelectionComponent |
| Description | The FeatureSelectionComponent is used for feature selection, verifying the validity of members and features. Horizontal modeling requires consistent features, generating task parameters and handling input/output. The task will be terminated if there are no features or if member matching fails. |


### UML Class Diagram

```mermaid
classDiagram
    class AbstractComponent~T~ {
        <<abstract>>
        +AbstractComponent()
        #checkBeforeBuildTask(FlowGraph graph, List~TaskMySqlModel~ preTasks, FlowGraphNode node, T params) void
        #createTaskParams(JobBuilder jobBuilder, FlowGraph graph, List~TaskMySqlModel~ preTasks, FlowGraphNode node, T params) JSONObject
        #getAllResult(String taskId) List~TaskResultMySqlModel~
        #getResult(String taskId, String type) TaskResultMySqlModel
        #inputs(FlowGraph graph, FlowGraphNode node) List~InputMatcher~
        +outputs(FlowGraph graph, FlowGraphNode node) List~OutputItem~
        +stopCreateTask(List~FlowGraphNode~ preNodes, FlowGraphNode node) boolean
        +taskType() ComponentType
    }

    class FeatureSelectionComponent {
        +FeatureSelectionComponent()
        +canSelectFeatures() boolean
        -Params params
        +stopCreateTask(List~FlowGraphNode~ preNodes, FlowGraphNode node) boolean
        #checkBeforeBuildTask(FlowGraph graph, List~TaskMySqlModel~ preTasks, FlowGraphNode node, Params params) void
        +taskType() ComponentType
        #createTaskParams(JobBuilder jobBuilder, FlowGraph graph, List~TaskMySqlModel~ preTasks, FlowGraphNode node, Params params) JSONObject
        #getAllResult(String taskId) List~TaskResultMySqlModel~
        #getResult(String taskId, String type) TaskResultMySqlModel
        #inputs(FlowGraph graph, FlowGraphNode node) List~InputMatcher~
        +outputs(FlowGraph graph, FlowGraphNode node) List~OutputItem~
    }

    class Params {
        -List~MemberFeatureInfoModel~ members
        +getMembers() List~MemberFeatureInfoModel~
        +setMembers(List~MemberFeatureInfoModel~ members) void
    }

    class MemberFeatureInfoModel {
        <<Model>>
        +getMemberId() String
        +getMemberRole() Enum
        +getFeatures() List~Feature~
    }

    class FlowGraphNode {
        <<Node>>
        +getParamsModel() Object
    }

    class DataIOComponent {
        <<Component>>
        +Params getParamsModel()
    }

    class FlowNodeException {
        <<Exception>>
    }

    AbstractComponent~T~ <|-- FeatureSelectionComponent
    FeatureSelectionComponent *-- Params
    Params o-- MemberFeatureInfoModel
    FeatureSelectionComponent --> FlowGraphNode : uses
    FeatureSelectionComponent --> DataIOComponent : queries
    FeatureSelectionComponent ..> FlowNodeException : throws
```

Class diagram description: This diagram illustrates the class structure of a feature selection component (FeatureSelectionComponent) that inherits from the generic abstract class AbstractComponent, containing an internal Params class for storing member feature information. The component retrieves parameters through FlowGraphNode, interacts with DataIOComponent for data validation, and throws FlowNodeException when validation fails. Core functionalities include task creation control, parameter validation, and result processing, supporting feature consistency checks for horizontal federated learning.


### Internal Method Call Graph

```mermaid
graph TD
    A["FeatureSelectionComponent"]
    B["Method: stopCreateTask"]
    C["Method: checkBeforeBuildTask"]
    D["Method: taskType"]
    E["Method: createTaskParams"]
    F["Method: getAllResult"]
    G["Method: getResult"]
    H["Method: inputs"]
    I["Method: outputs"]
    J["Method: canSelectFeatures"]
    K["Inner Class: Params"]

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

    B --> B1["Check if params.members is empty"]
    B1 -->|Yes| B2["Return true"]
    B1 -->|No| B3["Iterate members to check features"]
    B3 -->|Features selected| B4["Return false"]
    B3 -->|No features selected| B5["Return true"]

    C --> C1["Get DataIO node parameters"]
    C1 --> C2["Validate member participation consistency"]
    C2 -->|Mismatch| C3["Throw FlowNodeException"]
    C2 -->|Match| C4["Check horizontal federated feature consistency"]
    C4 -->|Inconsistent| C5["Throw FlowNodeException"]

    E --> E1["Reorganize member feature parameters"]
    E1 --> E2["Construct JSON output object"]
```

```mermaid
sequenceDiagram
    participant A as stopCreateTask
    participant B as checkBeforeBuildTask
    participant C as createTaskParams
    participant D as DataIOComponent

    A->>A: Check params.members
    alt members empty
        A-->>Caller: Return true
    else members not empty
        A->>A: Iterate to check features
        alt features selected
            A-->>Caller: Return false
        else no features selected
            A-->>Caller: Return true
        end
    end

    B->>D: Get DataIO node parameters
    D-->>B: Return dataSetItems
    B->>B: Validate member count
    alt count mismatch
        B-->>Caller: Throw exception
    else match
        B->>B: Check horizontal federated features
        alt features inconsistent
            B-->>Caller: Throw exception
        end
    end

    C->>C: Reorganize member feature parameters
    C->>C: Construct JSON object
    C-->>Caller: Return output
```

This code implements a feature selection component with three core methods: stopCreateTask validates whether features are selected to determine if task creation should be stopped; checkBeforeBuildTask performs data consistency validation before task construction; createTaskParams reorganizes feature parameters to generate task JSON. The flowchart shows the class structure and method invocation relationships, while the sequence diagram details the execution logic and data flow of key methods. The component emphasizes data consistency verification in federated learning scenarios, ensuring all participating parties have identical feature lists for horizontal modeling.

### Field List

| Name  | Type  | Description |
|-------|-------|------|

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| createTaskParams | JSONObject | The method restructures front-end parameters into a JSON object, iterates through the member list, extracts each member's ID, role, and feature name, and ultimately returns a JSON structure containing all member information. |
| inputs | List<InputMatcher> | Method override, returns an input matcher list containing dataset instances. |
| checkBeforeBuildTask | void | Check preconditions for build task: Ensure all members participate and the horizontal modeling feature list is consistent, otherwise throw an exception. |
| canSelectFeatures | boolean | The method canSelectFeatures returns true, indicating that selection functionality is supported. |
| getResult | TaskResultMySqlModel | This is a Java method that overrides the parent class method to retrieve results based on task ID and type, currently returning null. |
| getAllResult | List<TaskResultMySqlModel> | This is a Java method that overrides the parent class method, retrieving a list of all task results for a specified taskId by invoking the listAllResult method of taskResultService. |
| stopCreateTask | boolean | The method checks whether features are selected in the node parameters and stops task creation if none are selected or the member is empty. |
| outputs | List<OutputItem> | This method overrides the parent class method and returns a list containing an OutputItem, which consists of NORMAL_DATA_SET and DataSetInstance types. |
| taskType | ComponentType | The method returns the component type as feature selection. |




