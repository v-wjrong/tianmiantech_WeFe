# Basic Information

|      |      |
|------|------|
| Name | UpdateApi |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/api/project/node/UpdateApi.java |
| Package Name | com.welab.wefe.board.service.api.project.node |
| Dependencies | ['com.welab.wefe.board.service.component.Components', 'com.welab.wefe.board.service.component.DataIOComponent', 'com.welab.wefe.board.service.component.EvaluationComponent', 'com.welab.wefe.board.service.component.enums.EvaluationType', 'com.welab.wefe.board.service.dto.entity.job.ProjectFlowNodeOutputModel', 'com.welab.wefe.board.service.dto.vo.data_set.table_data_set.LabelDistribution', 'com.welab.wefe.board.service.exception.FlowNodeException', 'com.welab.wefe.board.service.model.FlowGraph', 'com.welab.wefe.board.service.model.FlowGraphNode', 'com.welab.wefe.board.service.service.JobService', 'com.welab.wefe.board.service.service.ProjectFlowNodeService', 'com.welab.wefe.board.service.service.data_resource.table_data_set.TableDataSetService', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.fieldvalidate.annotation.Check', 'com.welab.wefe.common.web.api.base.AbstractApi', 'com.welab.wefe.common.web.api.base.Api', 'com.welab.wefe.common.web.dto.AbstractApiInput', 'com.welab.wefe.common.web.dto.ApiResult', 'com.welab.wefe.common.wefe.enums.ComponentType', 'org.springframework.beans.factory.annotation.Autowired', 'java.util.Arrays', 'java.util.List', 'java.util.stream.Collectors'] |
| Brief Description | API class for updating node information, which checks whether the evaluation component matches the number of dataset categories and provides alerts if they do not match. The input includes process ID, node ID, component type, and parameters, and the output is a node list. |

# Description

The code defines an API class named `UpdateApi`, which is used to update project workflow node information. The API path is `project/flow/node/update`, inheriting from `AbstractApi`, and processes the input `Input` and output `Output`. Its primary functions include: updating workflow nodes via `projectFlowNodeService`, and checking whether the number of classifications matches the evaluation component's selected mode when editing the workflow. The validation logic involves constructing a `graph`, traversing evaluation components, and verifying the consistency between the dataset's classification count and the evaluation mode, throwing an exception with a prompt if they do not match. The input class `Input` includes fields such as workflow ID, node ID, component type, and parameters, along with validity checks. The output class `Output` contains a list of workflow nodes with empty parameters.

# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| UpdateApi | class | API class for updating node information, including input/output processing and evaluation of component-dataset matching check logic. |



## Class UpdateApi

|      |      |
|------|------|
| Access Modifier | @Api(path = "project/flow/node/update", name = "update node info");public |
| Type | class |
| Name | UpdateApi |
| Description | API class for updating node information, including input/output processing and evaluation of component-dataset matching check logic. |


### UML Class Diagram

```mermaid
classDiagram
    class UpdateApi {
        -ProjectFlowNodeService projectFlowNodeService
        -JobService jobService
        -TableDataSetService tableDataSetService
        +handle(Input input) ApiResult~Output~
        -check(Input input) void
        +checkByEvaluationNode(FlowGraph graph, FlowGraphNode evaluationNode) void
    }

    class AbstractApi~I, O~ {
        <<Abstract>>
        +handle(I input) ApiResult~O~
    }

    class Input {
        -String flowId
        -String nodeId
        -ComponentType componentType
        -String params
        +checkAndStandardize() void
        // getters/setters omitted for brevity
    }

    class Output {
        -List~ProjectFlowNodeOutputModel~ paramsIsNullFlowNodes
        // getters/setters omitted for brevity
    }

    class ProjectFlowNodeService {
        +updateFlowNode(Input input) List~ProjectFlowNodeOutputModel~
    }

    class JobService {
        +createFlowGraph(String flowId) FlowGraph
    }

    class TableDataSetService {
        +findOneById(String dataSetId) TableDataSet
    }

    class FlowGraph {
        +getAllJobSteps() List~FlowGraphNode~
        +findOneNodeFromParent(FlowGraphNode node, ComponentType type) FlowGraphNode
    }

    class FlowGraphNode {
        +getComponentType() ComponentType
        +getParamsModel() Object
    }

    class Components {
        <<Static>>
        +get(ComponentType type) Component
    }

    class Component {
        +deserializationParam(String params) Object
    }

    class TableDataSet {
        +getLabelDistribution() JsonObject
    }

    class LabelDistribution {
        +labelSpeciesCount int
    }

    UpdateApi --> AbstractApi~Input, Output~ : Inheritance
    UpdateApi --> ProjectFlowNodeService : Dependency
    UpdateApi --> JobService : Dependency
    UpdateApi --> TableDataSetService : Dependency
    Input --> Components : Dependency
    JobService --> FlowGraph : Creates
    TableDataSetService --> TableDataSet : Queries
    TableDataSet --> LabelDistribution : Contains
    FlowGraph --> FlowGraphNode : Contains
    Components --> Component : Association
```

The diagram illustrates the structural relationships of UpdateApi and its related classes. UpdateApi inherits from the generic abstract class AbstractApi and relies on three service classes to handle core business logic. The Input class is responsible for parameter validation, while the Output class encapsulates response data. The system collaborates through multiple service classes to complete flow node update operations, involving core functionalities such as flow graph construction, dataset queries, and component parameter validation. The class diagram clearly presents the collaborative relationships between components, particularly highlighting the flexible architectural design achieved through generics and interfaces.


### Internal Method Call Graph

```mermaid
graph TD
    A["UpdateApi Class"]
    B["Property: ProjectFlowNodeService"]
    C["Property: JobService"]
    D["Property: TableDataSetService"]
    E["Main Method: handle(Input input)"]
    F["Check Method: check(Input input)"]
    G["Node Check Method: checkByEvaluationNode(FlowGraph graph, FlowGraphNode evaluationNode)"]
    H["Inner Class: Input"]
    I["Inner Class: Output"]

    A --> B
    A --> C
    A --> D
    A --> E
    A --> F
    A --> G
    A --> H
    A --> I

    E -->|"1. Call projectFlowNodeService.updateFlowNode"| B
    E -->|"2. Call check(input)"| F
    E -->|"3. Return success(output)"| I

    F -->|"1. Check fromGateway"| H
    F -->|"2. Check componentType"| H
    F -->|"3. Create flowGraph"| C
    F -->|"4. Traverse evaluation nodes"| G

    G -->|"1. Get DataIO node"| C
    G -->|"2. Get dataset category count"| D
    G -->|"3. Check evaluation mode compatibility"| H
```

```mermaid
sequenceDiagram
    participant Client
    participant UpdateApi
    participant ProjectFlowNodeService
    participant JobService
    participant TableDataSetService

    Client->>UpdateApi: handle(input)
    UpdateApi->>ProjectFlowNodeService: updateFlowNode(input)
    ProjectFlowNodeService-->>UpdateApi: Return update result
    UpdateApi->>UpdateApi: check(input)
    UpdateApi->>JobService: createFlowGraph(flowId)
    JobService-->>UpdateApi: Return flowGraph
    loop Traverse evaluation nodes
        UpdateApi->>UpdateApi: checkByEvaluationNode(graph, node)
        UpdateApi->>JobService: findOneNodeFromParent()
        JobService-->>UpdateApi: Return dataIoNode
        UpdateApi->>TableDataSetService: findOneById(dataSetId)
        TableDataSetService-->>UpdateApi: Return labelSpeciesCount
    end
    UpdateApi-->>Client: Return success(output)
```

This code implements a flow node update API, with core functionalities including updating node information and validating the compatibility between evaluation components and datasets. The flowchart illustrates the class structure and method invocation relationships, while the sequence diagram details the complete call chain from client request to result return. The core validation logic involves traversing evaluation nodes in the flow graph to check if their category counts match with associated datasets. In case of mismatch, an exception is thrown to alert the user.

### Field List

| Name  | Type  | Description |
|-------|-------|------|
| projectFlowNodeService | ProjectFlowNodeService | Using @Autowired to automatically inject an instance of ProjectFlowNodeService. |
| tableDataSetService | TableDataSetService | Using @Autowired to automatically inject an instance of TableDataSetService. |
| jobService | JobService | Using @Autowired to automatically inject an instance of JobService. |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| handle | ApiResult<Output> | This method overrides the parent class logic, takes Input parameters, invokes the service to update the process node, and generates Output. After performing validation, it returns a successful result and may throw status code exceptions. |
| check | void | Check the input component type, only process DataIO and Evaluation types. If not initiated by a gateway, traverse all Evaluation nodes in the flowchart and validate them one by one. |
| checkByEvaluationNode | void | Check whether the number of evaluation nodes matches the dataset classification count. If the evaluation mode is binary classification but the dataset classification count exceeds 2, or if it is non-binary classification but the dataset classification count does not exceed 2, throw an exception indicating a mismatch. |




