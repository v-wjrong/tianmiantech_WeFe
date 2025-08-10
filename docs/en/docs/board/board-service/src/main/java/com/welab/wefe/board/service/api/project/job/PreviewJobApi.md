# Basic Information

|      |      |
|------|------|
| Name | PreviewJobApi |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/api/project/job/PreviewJobApi.java |
| Package Name | com.welab.wefe.board.service.api.project.job |
| Dependencies | ['com.welab.wefe.board.service.dto.entity.job.PreviewJobNodeOutputModel', 'com.welab.wefe.board.service.exception.FlowNodeException', 'com.welab.wefe.board.service.model.FlowGraph', 'com.welab.wefe.board.service.service.JobService', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.fieldvalidate.annotation.Check', 'com.welab.wefe.common.web.api.base.AbstractApi', 'com.welab.wefe.common.web.api.base.Api', 'com.welab.wefe.common.web.dto.AbstractApiInput', 'com.welab.wefe.common.web.dto.ApiResult', 'com.welab.wefe.common.web.util.ModelMapper', 'org.springframework.beans.factory.annotation.Autowired', 'java.util.List', 'java.util.stream.Collectors'] |
| Brief Description | API for previewing the execution process of a workflow. The input includes the workflow ID, whether to use cache, and termination nodes. The output includes cache result statistics and a detailed list of nodes. |

# Description

The PreviewJobApi is an API class designed for previewing workflow execution processes, inheriting from AbstractApi. It accepts input parameters including the workflow ID, whether to use cache, and the termination node ID. It utilizes JobService to create a workflow diagram and set cached results. During processing, workflow nodes are mapped to output models, with statistics collected for nodes with and without cache. Ultimately, it returns an output object containing statistical results and a node list. The input class Input includes validation and access methods for the workflow ID, cache usage flag, and termination node ID. The output class Output provides access methods for cache statistics and the node list.

# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| PreviewJobApi | class | The PreviewJobApi is used to preview the execution process of a workflow. The input includes the workflow ID, whether to use caching, and the termination node. The output contains cache result statistics and a detailed list of nodes. |



## Class PreviewJobApi

|      |      |
|------|------|
| Access Modifier | @Api(path = "project/flow/job/preview", name = "Preview flow execution process");public |
| Type | class |
| Name | PreviewJobApi |
| Description | The PreviewJobApi is used to preview the execution process of a workflow. The input includes the workflow ID, whether to use caching, and the termination node. The output contains cache result statistics and a detailed list of nodes. |


### UML Class Diagram

```mermaid
classDiagram
    class PreviewJobApi {
        -JobService jobService
        +handle(Input input) ApiResult~Output~
    }
    
    class AbstractApi~I, O~ {
        <<Abstract>>
        +handle(I input) ApiResult~O~
    }
    
    class JobService {
        +createFlowGraph(String flowId) FlowGraph
        +setGraphHasCacheResult(FlowGraph graph, boolean useCache) void
    }
    
    class FlowGraph {
        +getJobSteps(String endNodeId) List~JobStep~
    }
    
    class PreviewJobNodeOutputModel {
        +Object input
        +Object output
        +boolean hasCacheResult
        +getHasCacheResult() boolean
    }
    
    class Input {
        -String flowId
        -boolean useCache
        -String endNodeId
        +getFlowId() String
        +setFlowId(String flowId) void
        +isUseCache() boolean
        +setUseCache(boolean useCache) void
        +getEndNodeId() String
        +setEndNodeId(String endNodeId) void
    }
    
    class Output {
        -long hasCacheResultCount
        -long noCacheResultCount
        -List~PreviewJobNodeOutputModel~ list
        +getHasCacheResultCount() long
        +setHasCacheResultCount(long hasCacheResultCount) void
        +getNoCacheResultCount() long
        +setNoCacheResultCount(long noCacheResultCount) void
        +getList() List~PreviewJobNodeOutputModel~
        +setList(List~PreviewJobNodeOutputModel~ list) void
    }
    
    class AbstractApiInput {
        <<Abstract>>
    }
    
    PreviewJobApi --> AbstractApi~Input, Output~ : extends
    PreviewJobApi --> JobService : depends
    PreviewJobApi ..|> Input : contains
    PreviewJobApi ..|> Output : contains
    Input --> AbstractApiInput : extends
    JobService --> FlowGraph : creates
    FlowGraph --> JobStep : contains
    PreviewJobNodeOutputModel <-- Output : aggregates
```

Class Diagram Description: The diagram illustrates the structure of PreviewJobApi and its associated classes. PreviewJobApi inherits from the generic class AbstractApi and depends on JobService to create and process flow graphs. It contains nested classes Input and Output, where Input inherits from AbstractApiInput, and Output aggregates a list of PreviewJobNodeOutputModel. JobService interacts with FlowGraph, which contains JobStep information. The overall implementation provides flow execution preview functionality, including cache handling and data statistics capabilities.


### Internal Method Call Graph

```mermaid
graph TD
    A["Class PreviewJobApi"]
    B["Annotation: @Api"]
    C["Dependency Injection: JobService jobService"]
    D["Method: handle(Input input)"]
    E["Invocation: jobService.createFlowGraph"]
    F["Invocation: jobService.setGraphHasCacheResult"]
    G["Operation: graph.getJobSteps"]
    H["Stream Processing: map node transformation"]
    I["Exception Handling: catch FlowNodeException"]
    J["Statistics: Calculate cached node count"]
    K["Return: success(Output)"]
    L["Inner Class Input"]
    M["Inner Class Output"]

    A --> B
    A --> C
    A --> D
    D --> E
    D --> F
    D --> G
    G --> H
    H --> I
    D --> J
    D --> K
    A --> L
    A --> M
```

```mermaid
sequenceDiagram
    participant Client
    participant PreviewJobApi
    participant JobService
    participant FlowGraph
    participant ModelMapper

    Client->>PreviewJobApi: handle(input)
    PreviewJobApi->>JobService: createFlowGraph(flowId)
    JobService-->>PreviewJobApi: graph
    PreviewJobApi->>JobService: setGraphHasCacheResult(graph, useCache)
    PreviewJobApi->>FlowGraph: getJobSteps(endNodeId)
    loop Process each node
        FlowGraph->>ModelMapper: map(x, PreviewJobNodeOutputModel.class)
        ModelMapper-->>FlowGraph: model
        alt Get inputs/outputs
            FlowGraph->>Component: getInputs(graph, x)
            Component-->>FlowGraph: inputs
            FlowGraph->>Component: getOutputs(graph, x)
            Component-->>FlowGraph: outputs
        else Exception handling
            FlowGraph->>System.out: e.getMessage()
        end
    end
    PreviewJobApi->>PreviewJobApi: Count cached nodes
    PreviewJobApi-->>Client: success(output)
```

This code implements a workflow job preview API, whose primary function is to retrieve a flow diagram via flowId, process node data, and track cache hit statistics. The class diagram illustrates the class structure and key method invocation relationships, while the sequence diagram details the complete processing flow from client request to result return, including critical steps such as flow graph creation, node transformation, input/output retrieval, and exception handling. The inner class Input encapsulates request parameters, and Output packages response data. The overall design demonstrates clear responsibility segregation and layered processing principles.

### Field List

| Name  | Type  | Description |
|-------|-------|------|
| jobService | JobService | Automatically inject JobService instances. |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| handle | ApiResult<Output> | Process input to generate flowchart node output, count the number of cached and non-cached results, and return them. |




