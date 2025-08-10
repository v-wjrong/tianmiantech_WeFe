# 基础信息

|      |      |
|------|------|
| 名称 | FieldInfoService |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/fusion/FieldInfoService.java |
| 包名 | com.welab.wefe.board.service.service.fusion |
| 依赖项 | ['com.welab.wefe.board.service.database.entity.fusion.FieldInfoMySqlModel', 'com.welab.wefe.board.service.database.repository.fusion.FieldInfoRepository', 'com.welab.wefe.board.service.service.AbstractService', 'com.welab.wefe.board.service.util.primarykey.FieldInfo', 'com.welab.wefe.common.data.mysql.Where', 'com.welab.wefe.common.data.mysql.enums.OrderBy', 'com.welab.wefe.common.web.util.ModelMapper', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.data.jpa.domain.Specification', 'org.springframework.stereotype.Service', 'org.springframework.transaction.annotation.Transactional', 'java.util', 'java.util.stream.Collectors'] |
| 概述说明 | FieldInfoService提供字段信息管理功能，包括查询字段列表、字段信息列表及批量保存字段信息，支持按businessId操作，使用事务确保数据一致性。 |

# 说明

该代码定义了一个名为FieldInfoService的服务类，继承自AbstractService。它通过FieldInfoRepository与数据库交互，提供三个核心功能：columnList方法根据业务ID获取字段列名集合；fieldInfoList方法返回映射后的字段信息列表；saveAll方法以事务方式保存字段信息列表，先删除旧数据再插入新数据。私有方法findByBusinessId构建查询条件，按业务ID和位置排序获取数据。类使用Spring的依赖注入和事务管理注解。

# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| FieldInfoService | class | FieldInfoService类提供字段信息管理功能，包括查询字段列表、按业务ID获取字段信息及批量保存字段数据。通过Repository操作数据库，支持事务回滚。 |



## 类 FieldInfoService

|      |      |
|------|------|
| 访问范围 | @Service;public |
| 类型 | class |
| 名称 | FieldInfoService |
| 说明 | FieldInfoService类提供字段信息管理功能，包括查询字段列表、按业务ID获取字段信息及批量保存字段数据。通过Repository操作数据库，支持事务回滚。 |


### UML类图

```mermaid
classDiagram
    class AbstractService {
        <<Abstract>>
    }

    class FieldInfoService {
        -FieldInfoRepository fieldInfoRepository
        +Set~String~ columnList(String businessId)
        +List~FieldInfo~ fieldInfoList(String businessId)
        -List~FieldInfoMySqlModel~ findByBusinessId(String businessId)
        +void saveAll(String businessId, List~FieldInfo~ fieldInfoList)
    }

    class FieldInfoRepository {
        <<Interface>>
        +List~FieldInfoMySqlModel~ findAll(Specification~FieldInfoMySqlModel~ spec)
        +void deleteAll(List~FieldInfoMySqlModel~ entities)
        +void saveAll(List~FieldInfoMySqlModel~ entities)
    }

    class FieldInfoMySqlModel {
        -String businessId
        -String columns
        -String options
        -int fristIndex
        -int endIndex
        -int position
        +getters/setters
    }

    class FieldInfo {
        -String columns
        -String options
        -Integer fristIndex
        -Integer endIndex
        +getters/setters
    }

    class Where {
        <<Static>>
        +create() WhereBuilder
    }

    class ModelMapper {
        <<Static>>
        +map(Object source, Class~R~ destinationType) R
    }

    AbstractService <|-- FieldInfoService
    FieldInfoService --> FieldInfoRepository : 依赖
    FieldInfoService --> FieldInfoMySqlModel : 创建/操作
    FieldInfoService --> FieldInfo : 转换
    FieldInfoService ..> Where : 使用
    FieldInfoService ..> ModelMapper : 使用
    FieldInfoMySqlModel ..|> FieldInfo : 映射
```

该类图展示了FieldInfoService的核心结构及其关联关系。作为继承AbstractService的业务服务类，它通过FieldInfoRepository操作数据库，处理FieldInfoMySqlModel实体与FieldInfo数据传输对象之间的转换。借助Where构建查询条件，利用ModelMapper实现模型映射，主要提供字段列表查询、字段信息获取及批量保存功能，体现了典型的Spring数据访问层设计模式。


### 内部方法调用关系图

```mermaid
graph TD
    A["类FieldInfoService"]
    B["属性: FieldInfoRepository fieldInfoRepository"]
    C["方法: Set<String> columnList(String businessId)"]
    D["方法: List<FieldInfo> fieldInfoList(String businessId)"]
    E["私有方法: List<FieldInfoMySqlModel> findByBusinessId(String businessId)"]
    F["方法: void saveAll(String businessId, List<FieldInfo> fieldInfoList)"]
    G["操作: modelList = findByBusinessId(businessId)"]
    H["操作: 遍历modelList并分割columns字段"]
    I["操作: 返回Set<String> fields"]
    J["操作: modelList = findByBusinessId(businessId)"]
    K["操作: 流式处理并映射为FieldInfo列表"]
    L["操作: 返回List<FieldInfo>"]
    M["操作: 构建Specification查询条件"]
    N["操作: 执行repository查询并返回结果"]
    O["操作: 构建删除条件并执行删除"]
    P["操作: 创建新FieldInfoMySqlModel列表"]
    Q["操作: 遍历fieldInfoList填充模型数据"]
    R["操作: 执行批量保存"]

    A --> B
    A --> C
    A --> D
    A --> E
    A --> F
    C --> G
    G --> E
    C --> H
    C --> I
    D --> J
    J --> E
    D --> K
    D --> L
    E --> M
    E --> N
    F --> O
    O --> M
    O --> N
    F --> P
    F --> Q
    Q --> P
    F --> R
```

该流程图展示了FieldInfoService类的完整结构和方法调用关系。类包含核心的fieldInfoRepository属性和四个主要方法：columnList用于获取字段列集合，fieldInfoList用于获取字段信息列表，私有方法findByBusinessId实现公共查询逻辑，saveAll方法实现事务性的批量保存操作。流程清晰展示了各方法内部的处理步骤和相互调用关系，特别是saveAll方法包含删除旧数据和保存新数据的完整事务流程。所有方法都通过findByBusinessId方法复用查询逻辑，体现了良好的代码复用性。

### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| fieldInfoRepository | FieldInfoRepository | 自动注入FieldInfoRepository实例。 |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| columnList | Set<String> | 该方法根据业务ID查询字段信息，将每个模型的列名按逗号分割后合并到集合中，最终返回所有列名的唯一集合。 |
| findByBusinessId | List<FieldInfoMySqlModel> | 根据业务ID查询字段信息，按position升序排序并返回列表。 |
| saveAll | void | 事务方法saveAll：根据businessId删除旧数据，转换并保存新FieldInfo列表到数据库，异常时回滚。 |
| fieldInfoList | List<FieldInfo> | 该方法根据businessId查询FieldInfoMySqlModel列表，并通过流操作将其映射为FieldInfo列表后返回。 |




