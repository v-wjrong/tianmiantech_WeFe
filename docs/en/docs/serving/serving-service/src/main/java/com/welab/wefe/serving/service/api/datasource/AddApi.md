# Basic Information

|      |      |
|------|------|
| Name | AddApi |
| Language | .java |
| Code Path | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/api/datasource/AddApi.java |
| Package Name | com.welab.wefe.serving.service.api.datasource |
| Dependencies | ['com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.fieldvalidate.annotation.Check', 'com.welab.wefe.common.jdbc.base.DatabaseType', 'com.welab.wefe.common.web.api.base.AbstractApi', 'com.welab.wefe.common.web.api.base.Api', 'com.welab.wefe.common.web.dto.AbstractApiInput', 'com.welab.wefe.common.web.dto.AbstractApiOutput', 'com.welab.wefe.common.web.dto.ApiResult', 'com.welab.wefe.serving.service.service.DataSourceService', 'org.springframework.beans.factory.annotation.Autowired'] |
| Brief Description | Added a new data source API class to handle input parameters such as name, type, host, port, etc., invoking the service to add a data source and returning the ID. Input parameters require validation, with the name length between 4-30. |

# Description

The code defines an API class named `AddApi`, which is used to add a new data source. The API path is `data_source/add`, accepting the `DataSourceAddInput` as the input parameter and returning the `DataSourceAddOutput` as the output result. The input parameters include mandatory fields such as the data source name, database type, IP address, port, database name, username, and password, where the name must adhere to a length constraint of 4-30 characters. The output parameter contains the generated ID. The `DataSourceService` processes the addition request and returns the operation result.

# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| AddApi | class | Added a new data source API class to handle data source addition requests. The input includes required fields such as ID, name, database type, host, port, database name, username, and password. The output returns the generated ID. The addition logic is implemented through the DataSourceService. |



## Class AddApi

|      |      |
|------|------|
| Access Modifier | @Api(path = "data_source/add", name = "新增数据源");public |
| Type | class |
| Name | AddApi |
| Description | Added a new data source API class to handle data source addition requests. The input includes required fields such as ID, name, database type, host, port, database name, username, and password. The output returns the generated ID. The addition logic is implemented through the DataSourceService. |


### UML Class Diagram

```mermaid
classDiagram
    class AbstractApi~T, R~ {
        <<abstract>>
        +handle(T input) ApiResult~R~
    }

    class AddApi {
        -DataSourceService dataSourceService
        +handle(DataSourceAddInput input) ApiResult~DataSourceAddOutput~
    }

    class DataSourceAddInput {
        -String id
        -String name
        -DatabaseType databaseType
        -String host
        -Integer port
        -String databaseName
        -String userName
        -String password
        +getName() String
        +setName(String name) void
        // ...Other getter/setter methods
    }

    class DataSourceAddOutput {
        -String id
        +getId() String
        +setId(String id) void
    }

    class DataSourceService {
        +add(DataSourceAddInput input) DataSourceAddOutput
    }

    class DatabaseType {
        <<enumeration>>
    }

    AbstractApi~T, R~ <|-- AddApi : Inheritance
    AddApi --> DataSourceService : Dependency
    AddApi *-- DataSourceAddInput : Composition
    AddApi *-- DataSourceAddOutput : Composition
    DataSourceAddInput --> DatabaseType : Usage
```

This code demonstrates an API implementation for adding data sources, adopting a layered architecture design. The AddApi inherits from the generic abstract class AbstractApi, processes DataSourceAddInput and returns DataSourceAddOutput. The input class contains various data source parameters and validation annotations, while the output class simply encapsulates the generated ID. The core business logic is handled through the dependency-injected DataSourceService, reflecting a clear separation of responsibilities and type-safe design philosophy.


### Internal Method Call Graph

```mermaid
graph TD
    A["Class AddApi"]
    B["Annotation: @Api"]
    C["Inheritance: AbstractApi<DataSourceAddInput, DataSourceAddOutput>"]
    D["Dependency Injection: @Autowired DataSourceService"]
    E["Overridden Method: handle(DataSourceAddInput input)"]
    F["Inner Class: DataSourceAddInput"]
    G["Inner Class: DataSourceAddOutput"]
    H["Method Call: dataSourceService.add(input)"]
    I["Return Result: success()"]

    A --> B
    A --> C
    A --> D
    A --> E
    A --> F
    A --> G
    E --> H
    H --> I

    subgraph DataSourceAddInput
        F1["Property: String id"]
        F2["Property: String name"]
        F3["Property: DatabaseType databaseType"]
        F4["Property: String host"]
        F5["Property: Integer port"]
        F6["Property: String databaseName"]
        F7["Property: String userName"]
        F8["Property: String password"]
        F9["Validation Annotation: @Check"]
        F10["Getter/Setter Methods"]
    end

    subgraph DataSourceAddOutput
        G1["Property: String id"]
        G2["Getter/Setter Methods"]
    end
```

This code demonstrates an API class AddApi for adding data sources, which inherits from the abstract class AbstractApi and implements the core processing method handle. The API includes two nested static classes: DataSourceAddInput defines the input parameter structure with multiple validation annotations, while DataSourceAddOutput defines a simple output structure. The flowchart clearly presents the class inheritance relationship, dependency injection, method call chain, and the attribute structure of inner classes, fully reflecting the data processing flow from input to output.

### Field List

| Name  | Type  | Description |
|-------|-------|------|
| dataSourceService | DataSourceService | Using @Autowired to automatically inject a DataSourceService instance. |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| handle | ApiResult<DataSourceAddOutput> | Java method overriding, handling data source addition requests, calling service layer methods and returning results. |




