# 基础信息

|      |      |
|------|------|
| 名称 | OperationLogService |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/OperationLogService.java |
| 包名 | com.welab.wefe.board.service.service |
| 依赖项 | ['com.welab.wefe.board.service.api.operation.LogQueryApi', 'com.welab.wefe.board.service.database.entity.OperationLogMysqlModel', 'com.welab.wefe.board.service.database.repository.OperationLogRepository', 'com.welab.wefe.board.service.dto.base.PagingOutput', 'com.welab.wefe.board.service.dto.entity.OperationLogOutputModel', 'com.welab.wefe.common.data.mysql.Where', 'com.welab.wefe.common.data.mysql.enums.OrderBy', 'com.welab.wefe.common.exception.StatusCodeWithException', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.data.jpa.domain.Specification', 'org.springframework.stereotype.Service'] |
| 概述说明 | OperationLogService提供日志查询功能，支持按接口、操作者ID和时间范围筛选，并返回分页结果。 |

# 说明

OperationLogService是一个服务类，继承自AbstractService，用于处理操作日志查询。它通过Autowired注入OperationLogRepository依赖。主要方法query接收LogQueryApi.Input参数，返回分页的OperationLogOutputModel结果。查询条件包括logInterface和operatorId的精确匹配，createdTime的时间范围筛选，并按createdTime降序排序。最后调用mOperationLogRepository的paging方法执行分页查询。

# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| OperationLogService | class | OperationLogService提供分页查询操作日志功能，支持按接口、操作者ID和时间范围筛选，结果按创建时间降序排列。 |



## 类 OperationLogService

|      |      |
|------|------|
| 访问范围 | @Service;public |
| 类型 | class |
| 名称 | OperationLogService |
| 说明 | OperationLogService提供分页查询操作日志功能，支持按接口、操作者ID和时间范围筛选，结果按创建时间降序排列。 |


### UML类图

```mermaid
classDiagram
    class OperationLogService {
        -OperationLogRepository mOperationLogRepository
        +PagingOutput~OperationLogOutputModel~ query(LogQueryApi$Input input) StatusCodeWithException
    }
    class AbstractService {
        <<Abstract>>
    }
    class OperationLogRepository {
        <<Interface>>
        +paging(Specification~OperationLogMysqlModel~ where, LogQueryApi$Input input, Class~OperationLogOutputModel~ clazz) PagingOutput~OperationLogOutputModel~
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
        <<Interface>>
    }
    class Where {
        +create() WhereBuilder
    }
    class WhereBuilder {
        +equal(String field, Object value) WhereBuilder
        +betweenAndDate(String field, Date start, Date end) WhereBuilder
        +orderBy(String field, OrderBy order) WhereBuilder
        +build(Class~T~ clazz) Specification~T~
    }
    class OrderBy {
        <<Enumeration>>
        +asc
        +desc
    }

    OperationLogService --|> AbstractService : 继承
    OperationLogService --> OperationLogRepository : 依赖
    OperationLogService --> LogQueryApi : 依赖
    OperationLogService --> OperationLogOutputModel : 依赖
    OperationLogService --> PagingOutput~OperationLogOutputModel~ : 依赖
    OperationLogRepository --> Specification~OperationLogMysqlModel~ : 依赖
    OperationLogRepository --> OperationLogMysqlModel : 依赖
    Where --> WhereBuilder : 创建
    WhereBuilder --> Specification~OperationLogMysqlModel~ : 构建
    WhereBuilder --> OrderBy : 使用
```

该类图展示了OperationLogService及其相关组件的结构关系。OperationLogService继承自AbstractService，依赖OperationLogRepository进行数据访问，使用Where构建查询条件，并通过PagingOutput返回分页结果。核心功能是通过动态条件查询操作日志，支持等值匹配、时间范围查询和排序。各组件职责明确，WhereBuilder提供流畅的查询条件构建接口，Repository处理具体数据访问逻辑。


### 内部方法调用关系图

```mermaid
graph TD
    A["类OperationLogService"]
    B["继承: AbstractService"]
    C["依赖注入: OperationLogRepository"]
    D["方法: query(LogQueryApi.Input input)"]
    E["创建条件构造器: Where.create()"]
    F["添加条件: equal('logInterface', input.logInterface)"]
    G["添加条件: equal('operatorId', input.operatorId)"]
    H["添加时间范围: betweenAndDate('createdTime', input.startTime, input.endTime)"]
    I["添加排序: orderBy('createdTime', OrderBy.desc)"]
    J["构建条件: build(OperationLogMysqlModel.class)"]
    K["分页查询: mOperationLogRepository.paging(where, input, OperationLogOutputModel.class)"]

    A --> B
    A --> C
    A --> D
    D --> E
    E --> F
    F --> G
    G --> H
    H --> I
    I --> J
    J --> K
```

该流程图展示了OperationLogService类的核心查询流程。从创建条件构造器开始，逐步添加字段匹配条件、时间范围筛选和排序规则，最终通过Repository执行分页查询。整个过程严格遵循条件构造模式，将输入参数转换为数据库查询规范，体现了清晰的链式调用结构和数据过滤逻辑。

### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| mOperationLogRepository | OperationLogRepository | 使用@Autowired自动注入OperationLogRepository实例。 |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| query | PagingOutput<OperationLogOutputModel> | 查询操作日志方法，根据接口、操作者ID和时间范围筛选，按创建时间降序分页返回结果。 |




