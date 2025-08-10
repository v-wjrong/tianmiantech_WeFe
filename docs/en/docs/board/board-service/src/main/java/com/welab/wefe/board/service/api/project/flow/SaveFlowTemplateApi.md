# Basic Information

|      |      |
|------|------|
| Name | SaveFlowTemplateApi |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/api/project/flow/SaveFlowTemplateApi.java |
| Package Name | com.welab.wefe.board.service.api.project.flow |
| Dependencies | ['com.welab.wefe.board.service.service.FlowTemplateService', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.fieldvalidate.annotation.Check', 'com.welab.wefe.common.web.api.base.AbstractApi', 'com.welab.wefe.common.web.api.base.Api', 'com.welab.wefe.common.web.dto.AbstractApiInput', 'com.welab.wefe.common.web.dto.ApiResult', 'org.springframework.beans.factory.annotation.Autowired'] |
| Brief Description | API for saving process templates, which receives name, description, and flowchart inputs, invokes a service to generate a template ID and returns it. Includes input/output class definitions and core processing logic. |

# Description

This is an API class named SaveFlowTemplateApi, used for saving workflow templates. The API path is project/flow/template/save. It inherits from the AbstractApi class and utilizes FlowTemplateService to handle business logic. The input parameter Input includes the template name, description, and flowchart, all annotated with validation annotations. The output parameter Output contains the generated template ID. The processing logic involves adding the template via the flowTemplateService.addTemplate method and returning a successful result containing the template ID.

# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| SaveFlowTemplateApi | class | Save Process Template API, which receives name, description, and flowchart inputs, invokes the service to generate a template ID and returns it. |



## Class SaveFlowTemplateApi

|      |      |
|------|------|
| Access Modifier | @Api(path = "project/flow/template/save", name = "save flow template");public |
| Type | class |
| Name | SaveFlowTemplateApi |
| Description | Save Process Template API, which receives name, description, and flowchart inputs, invokes the service to generate a template ID and returns it. |


### UML Class Diagram

```mermaid
classDiagram
    class SaveFlowTemplateApi {
        -FlowTemplateService flowTemplateService
        +handle(Input input) ApiResult~Output~
    }
    class AbstractApi~Input, Output~ {
        <<Abstract>>
    }
    SaveFlowTemplateApi --|> AbstractApi~Input, Output~ : Extends

    class Output {
        -String templateId
        +Output(String templateId)
        +String getTemplateId()
        +void setTemplateId(String templateId)
    }

    class Input {
        -String name
        -String description
        -String graph
        +String getName()
        +void setName(String name)
        +String getDescription()
        +void setDescription(String description)
        +String getGraph()
        +void setGraph(String graph)
    }
    Input --|> AbstractApiInput : Extends

    class AbstractApiInput {
        <<Abstract>>
    }

    SaveFlowTemplateApi --> Input : Uses
    SaveFlowTemplateApi --> Output : Uses
    SaveFlowTemplateApi --> FlowTemplateService : Depends
```

This code demonstrates the class structure of a Save Flow Template API. SaveFlowTemplateApi inherits from the generic abstract class AbstractApi, defining two nested classes Input and Output as parameters. The Input class extends AbstractApiInput, containing fields like template name, description, and flow graph; the Output class includes the generated template ID. The API processes business logic through the injected FlowTemplateService, transforming input into output results. The overall design reflects clear separation of responsibilities and layered architecture.


### Internal Method Call Graph

```mermaid
graph TD
    A["Class SaveFlowTemplateApi"]
    B["Annotation: @Api"]
    C["Dependency Injection: FlowTemplateService"]
    D["Method: handle(Input input)"]
    E["Inner Class Output"]
    F["Inner Class Input"]
    G["Method: addTemplate(input)"]
    H["Method: success(new Output(templateId))"]
    I["Property: String templateId"]
    J["Property: String name"]
    K["Property: String description"]
    L["Property: String graph"]

    A --> B
    A --> C
    A --> D
    A --> E
    A --> F
    D --> G
    D --> H
    E --> I
    F --> J
    F --> K
    F --> L
```

This flowchart illustrates the structure of the SaveFlowTemplateApi class, including the main class, annotations, dependency-injected service, core processing method handle, and two inner classes Output and Input. The handle method processes input via flowTemplateService.addTemplate and returns a successful result containing the template ID. The Input class includes three validated properties: template name, description, and flowchart, while the Output class encapsulates the generated template ID. The entire process clearly reflects the data flow path of API request handling.

### Field List

| Name  | Type  | Description |
|-------|-------|------|
| flowTemplateService | FlowTemplateService | Automatically inject the process template service instance. |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| handle | ApiResult<Output> | The method processes the input and invokes the service to add a template, returning a successful result containing the template ID. |




