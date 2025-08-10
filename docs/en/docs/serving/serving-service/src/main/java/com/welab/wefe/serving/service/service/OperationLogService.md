# Basic Information

|      |      |
|------|------|
| Name | OperationLogService |
| Language | .java |
| Code Path | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/service/OperationLogService.java |
| Package Name | com.welab.wefe.serving.service.service |
| Dependencies | ['com.welab.wefe.common.data.mysql.Where', 'com.welab.wefe.common.data.mysql.enums.OrderBy', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.serving.service.api.operation.LogQueryApi', 'com.welab.wefe.serving.service.database.entity.OperationLogMysqlModel', 'com.welab.wefe.serving.service.database.repository.OperationLogRepository', 'com.welab.wefe.serving.service.dto.OperationLogOutputModel', 'com.welab.wefe.serving.service.dto.PagingOutput', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.data.jpa.domain.Specification', 'org.springframework.stereotype.Service'] |
| Brief Description | Operation log service class, which queries logs based on input conditions, supports pagination, interface, operator ID, and time range filtering, with results sorted in descending order by time. |

# Description

OperationLogService is a service class used for querying operation logs. It relies on OperationLogRepository for database operations. The query method accepts a LogQueryApi.Input parameter, constructs query conditions including filtering by interface name and operator ID, as well as sorting by time range. The query results are returned in paginated form as OperationLogOutputModel objects. The method may throw a StatusCodeWithException.

# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| OperationLogService | class | OperationLogService provides the functionality to query operation logs, supporting filtering by interface, operator ID, and time range, with results paginated and returned in descending order of creation time. |



## Class OperationLogService

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | OperationLogService |
| Description | OperationLogService provides the functionality to query operation logs, supporting filtering by interface, operator ID, and time range, with results paginated and returned in descending order of creation time. |


### UML Class Diagram

```mermaid
classDiagram
    class OperationLogService {
        -OperationLogRepository mOperationLogRepository
        +PagingOutput~OperationLogOutputModel~ query(LogQueryApi$Input input) StatusCodeWithException
    }

    class OperationLogRepository {
        +PagingOutput~OperationLogOutputModel~ paging(Specification~OperationLogMysqlModel~ where, LogQueryApi$Input input, Class~OperationLogOutputModel~ clazz)
    }

    class LogQueryApi {
        <<Interface>>
    }

    class OperationLogMysqlModel {
    }

    class OperationLogOutputModel {
    }

    class PagingOutput~T~ {
    }

    class Specification~T~ {
    }

    class Where {
        +equal(String field, Object value) Where
        +betweenAndDate(String field, Date start, Date end) Where
        +orderBy(String field, OrderBy order) Where
        +build(Class~T~ clazz) Specification~T~
    }

    class OrderBy {
        <<Enumeration>>
        +asc
        +desc
    }

    OperationLogService --> OperationLogRepository : Dependency
    OperationLogService --> LogQueryApi : Dependency
    OperationLogService --> OperationLogMysqlModel : Dependency
    OperationLogService --> OperationLogOutputModel : Dependency
    OperationLogService --> PagingOutput : Dependency
    OperationLogService --> Where : Dependency
    Where --> Specification : Creates
    Where --> OrderBy : Uses
    OperationLogRepository --> Specification : Dependency
    OperationLogRepository --> OperationLogMysqlModel : Dependency
    OperationLogRepository --> OperationLogOutputModel : Dependency
    OperationLogRepository --> PagingOutput : Dependency
```

This code illustrates an operation log query service, with OperationLogService as the core class that performs paginated queries through OperationLogRepository using the Where builder to construct query conditions. The class diagram clearly depicts relationships between components: the service layer depends on the repository layer and query condition builder, the repository handles concrete data queries and pagination operations, while the Where class is responsible for building complex query specifications. The design exemplifies layered architecture and the application of the specification pattern.


### Internal Method Call Graph

```mermaid
graph TD
    A["Class OperationLogService"]
    B["Dependency Injection: OperationLogRepository"]
    C["Method: query(LogQueryApi.Input input)"]
    D["Create Specification: Where.create()"]
    E["Add condition: equal('logInterface', input.logInterface)"]
    F["Add condition: equal('operatorId', input.operatorId)"]
    G["Add time range condition: betweenAndDate('createdTime', input.getStartTime(), input.getEndTime())"]
    H["Add sorting: orderBy('createdTime', OrderBy.desc)"]
    I["Build condition: build(OperationLogMysqlModel.class)"]
    J["Execute paginated query: mOperationLogRepository.paging(where, input, OperationLogOutputModel.class)"]
    K["Return result: PagingOutput<OperationLogOutputModel>"]

    A --> B
    A --> C
    C --> D
    D --> E
    D --> F
    D --> G
    D --> H
    D --> I
    C --> J
    J --> K
```

This code flowchart illustrates the core query process of the OperationLogService class. The service obtains a log repository instance via dependency injection, constructs a multi-condition query specification including interface name, operator ID, and time range in the query method, and finally retrieves results through the repository's pagination method. The entire process demonstrates the complete chain from condition assembly to database query, with the Where builder pattern clearly showing the logical hierarchy of dynamic condition combination.

### Field List

| Name  | Type  | Description |
|-------|-------|------|
| mOperationLogRepository | OperationLogRepository | Using @Autowired to automatically inject an instance of OperationLogRepository. |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| query | PagingOutput<OperationLogOutputModel> | Query operation log method, filter logs based on input conditions including interface, operator ID, and time range, and return results in descending order of creation time with pagination. |




