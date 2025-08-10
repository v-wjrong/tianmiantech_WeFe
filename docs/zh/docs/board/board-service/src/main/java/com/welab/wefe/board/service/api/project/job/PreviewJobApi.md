# 基础信息

|      |      |
|------|------|
| 名称 | PreviewJobApi |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/api/project/job/PreviewJobApi.java |
| 包名 | com.welab.wefe.board.service.api.project.job |
| 依赖项 | ['com.welab.wefe.board.service.dto.entity.job.PreviewJobNodeOutputModel', 'com.welab.wefe.board.service.exception.FlowNodeException', 'com.welab.wefe.board.service.model.FlowGraph', 'com.welab.wefe.board.service.service.JobService', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.fieldvalidate.annotation.Check', 'com.welab.wefe.common.web.api.base.AbstractApi', 'com.welab.wefe.common.web.api.base.Api', 'com.welab.wefe.common.web.dto.AbstractApiInput', 'com.welab.wefe.common.web.dto.ApiResult', 'com.welab.wefe.common.web.util.ModelMapper', 'org.springframework.beans.factory.annotation.Autowired', 'java.util.List', 'java.util.stream.Collectors'] |
| 概述说明 | 预览流程执行过程的API，输入包含流程ID、是否使用缓存和终止节点，输出包含缓存结果统计和节点详情列表。 |

# 说明

PreviewJobApi是一个用于预览流程执行过程的API类，继承自AbstractApi。它接收包含流程ID、是否使用缓存和终止节点ID的输入参数，通过JobService创建流程图并设置缓存结果。处理过程中，将流程节点映射为输出模型，统计有缓存和无缓存的节点数量，最终返回包含统计结果和节点列表的输出对象。输入类Input包含流程ID、是否使用缓存和终止节点ID的校验和访问方法。输出类Output包含缓存统计数据和节点列表的访问方法。

# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| PreviewJobApi | class | PreviewJobApi用于预览流程执行过程，输入包括流程ID、是否使用缓存和终止节点，输出包含缓存结果统计和节点详情列表。 |



## 类 PreviewJobApi

|      |      |
|------|------|
| 访问范围 | @Api(path = "project/flow/job/preview", name = "Preview flow execution process");public |
| 类型 | class |
| 名称 | PreviewJobApi |
| 说明 | PreviewJobApi用于预览流程执行过程，输入包括流程ID、是否使用缓存和终止节点，输出包含缓存结果统计和节点详情列表。 |


### UML类图

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
    
    PreviewJobApi --> AbstractApi~Input, Output~ : 继承
    PreviewJobApi --> JobService : 依赖
    PreviewJobApi ..|> Input : 包含
    PreviewJobApi ..|> Output : 包含
    Input --> AbstractApiInput : 继承
    JobService --> FlowGraph : 创建
    FlowGraph --> JobStep : 包含
    PreviewJobNodeOutputModel <-- Output : 聚合
```

类图描述：该图展示了PreviewJobApi及其关联类的结构。PreviewJobApi继承自泛型类AbstractApi，依赖JobService来创建和处理流程图。包含嵌套类Input和Output，其中Input继承自AbstractApiInput，Output聚合了PreviewJobNodeOutputModel列表。JobService与FlowGraph交互，后者包含JobStep信息。整体实现了流程执行预览功能，包含缓存处理和数据统计能力。


### 内部方法调用关系图

```mermaid
graph TD
    A["类PreviewJobApi"]
    B["注解: @Api"]
    C["依赖注入: JobService jobService"]
    D["方法: handle(Input input)"]
    E["调用: jobService.createFlowGraph"]
    F["调用: jobService.setGraphHasCacheResult"]
    G["操作: graph.getJobSteps"]
    H["流处理: map节点转换"]
    I["异常处理: catch FlowNodeException"]
    J["统计: 计算缓存节点数量"]
    K["返回: success(Output)"]
    L["内部类Input"]
    M["内部类Output"]

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
    loop 处理每个节点
        FlowGraph->>ModelMapper: map(x, PreviewJobNodeOutputModel.class)
        ModelMapper-->>FlowGraph: model
        alt 获取输入输出
            FlowGraph->>Component: getInputs(graph, x)
            Component-->>FlowGraph: inputs
            FlowGraph->>Component: getOutputs(graph, x)
            Component-->>FlowGraph: outputs
        else 异常处理
            FlowGraph->>System.out: e.getMessage()
        end
    end
    PreviewJobApi->>PreviewJobApi: 统计缓存节点
    PreviewJobApi-->>Client: success(output)
```

这段代码实现了一个流程作业预览API，主要功能是通过flowId获取流程图，处理节点数据并统计缓存命中情况。流程图展示了类结构和主要方法调用关系，时序图详细描述了从客户端请求到返回结果的完整处理过程，包括流程图创建、节点转换、输入输出获取以及异常处理等关键步骤。内部类Input用于封装请求参数，Output用于包装响应数据，整个设计体现了清晰的职责划分和分层处理思想。

### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| jobService | JobService | 自动注入JobService实例。 |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| handle | ApiResult<Output> | 处理输入生成流程图节点输出，统计缓存与非缓存结果数量并返回。 |




