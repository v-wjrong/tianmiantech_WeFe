# 基础信息

|      |      |
|------|------|
| 名称 | JobMemberService |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/JobMemberService.java |
| 包名 | com.welab.wefe.board.service.service |
| 依赖项 | ['com.alibaba.fastjson.JSONArray', 'com.welab.wefe.board.service.database.entity.job.JobMemberMySqlModel', 'com.welab.wefe.board.service.database.repository.JobMemberRepository', 'com.welab.wefe.board.service.dto.entity.job.JobMemberOutputModel', 'com.welab.wefe.common.data.mysql.Where', 'com.welab.wefe.common.web.util.ModelMapper', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.data.domain.Sort', 'org.springframework.data.jpa.domain.Specification', 'org.springframework.stereotype.Service', 'java.util.List', 'java.util.stream.Collectors'] |
| 概述说明 | JobMemberService提供任务成员查询功能，包括按任务ID获取成员列表、排除仲裁者、条件组合查询及本地任务判断。 |

# 说明

JobMemberService是一个服务类，提供与任务成员相关的操作。主要功能包括：获取任务成员列表，支持按角色过滤；通过任务ID、成员角色和成员ID查询单个成员；根据任务ID查询成员列表；检查任务是否为本地任务。方法使用Where条件构建查询，并通过Repository执行数据库操作。部分方法涉及并行流处理和模型映射转换。

# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| JobMemberService | class | JobMemberService提供作业成员管理功能，包括查询成员列表、按条件查找成员、检查本地作业等。支持按角色、ID等条件筛选，使用并行流处理数据转换。 |



## 类 JobMemberService

|      |      |
|------|------|
| 访问范围 | @Service;public |
| 类型 | class |
| 名称 | JobMemberService |
| 说明 | JobMemberService提供作业成员管理功能，包括查询成员列表、按条件查找成员、检查本地作业等。支持按角色、ID等条件筛选，使用并行流处理数据转换。 |


### UML类图

```mermaid
classDiagram
    class JobMemberService {
        -JobMemberRepository repo
        +List~JobMemberOutputModel~ list(String jobId)
        +List~JobMemberOutputModel~ list(String jobId, boolean includeArbiter)
        +JobMemberMySqlModel findIdByMemberInfo(String jobId, JobMemberRole myRole, String memberId)
        +JobMemberMySqlModel findOneByJobRole(String businessId, JobMemberRole jobRole, String memberId)
        +List~JobMemberMySqlModel~ findListByJobId(String jobId)
        +boolean isLocalJob(String jobId)
    }

    class JobMemberRepository {
        <<Interface>>
        +findAll(Specification~T~ spec, Sort sort) List~T~
        +query(String sql) List~Object[]~
        +findById(String id) Optional~T~
        +findOne(Specification~T~ spec) Optional~T~
        +count(Specification~T~ spec) long
    }

    class Where {
        <<Interface>>
        +create() Where
        +equal(String field, Object value) Where
        +notEqual(String field, Object value) Where
        +build(Class~T~ clazz) Specification~T~
    }

    class JobMemberOutputModel {
        // 数据输出模型
    }

    class JobMemberMySqlModel {
        // 数据库实体模型
    }

    class JobMemberRole {
        <<Enumeration>>
        arbiter
        // 其他角色值
    }

    JobMemberService --> JobMemberRepository : 依赖
    JobMemberService --> Where : 依赖
    JobMemberService --> JobMemberOutputModel : 返回
    JobMemberService --> JobMemberMySqlModel : 返回/查询
    JobMemberService --> JobMemberRole : 使用
    Where --> Specification : 生成
```

该代码展示了一个作业成员服务类(JobMemberService)，主要提供作业成员相关的数据库操作功能。类图清晰地呈现了服务类与仓库接口(JobMemberRepository)、条件构造器(Where)、数据模型(JobMemberOutputModel/JobMemberMySqlModel)以及枚举类型(JobMemberRole)之间的关系。服务类通过仓库接口进行数据访问，使用Where构建查询条件，处理两种不同的数据模型，并利用枚举类型区分成员角色。其中包含列表查询、条件查询、本地作业判断等多种业务方法，体现了完整的成员管理功能。


### 内部方法调用关系图

```mermaid
graph TD
    A["类JobMemberService"]
    B["属性: JobMemberRepository repo"]
    C["方法: list(String jobId)"]
    D["方法: list(String jobId, boolean includeArbiter)"]
    E["方法: findIdByMemberInfo(String jobId, JobMemberRole myRole, String memberId)"]
    F["方法: findOneByJobRole(String businessId, JobMemberRole jobRole, String memberId)"]
    G["方法: findListByJobId(String jobId)"]
    H["方法: isLocalJob(String jobId)"]
    I["Where条件构造"]
    J["数据库查询操作"]
    K["结果映射/处理"]

    A --> B
    A --> C
    A --> D
    A --> E
    A --> F
    A --> G
    A --> H
    C --> D
    D --> I --> J --> K
    E --> J --> K
    F --> I --> J --> K
    G --> I --> J --> K
    H --> I --> J --> K
```

```mermaid
sequenceDiagram
    participant Client
    participant JobMemberService
    participant JobMemberRepository
    participant Where
    participant ModelMapper

    Client->>JobMemberService: list(jobId)
    JobMemberService->>JobMemberService: list(jobId, true)
    JobMemberService->>Where: create().equal('jobId', jobId)
    Where-->>JobMemberService: where条件
    JobMemberService->>JobMemberRepository: findAll(where.build())
    JobMemberRepository-->>JobMemberService: List<JobMemberMySqlModel>
    JobMemberService->>ModelMapper: parallelStream().map(x->map(x))
    ModelMapper-->>JobMemberService: Stream<JobMemberOutputModel>
    JobMemberService->>JobMemberService: collect(Collectors.toList())
    JobMemberService-->>Client: List<JobMemberOutputModel>
```

这段代码是JobMemberService服务类，主要处理与工作成员相关的业务逻辑。它提供了多种查询方法，包括获取成员列表、根据条件查询单个成员、查询成员列表以及判断是否为本地工作等。核心流程是通过Where类构建查询条件，然后调用Repository进行数据库操作，最后对结果进行映射或处理。特别注意包含并行流处理和条件过滤等高级特性，体现了对性能和数据完整性的考虑。

### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| repo | JobMemberRepository | 自动注入JobMemberRepository实例到repo变量。 |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| list | List<JobMemberOutputModel> | 方法根据jobId查询任务成员列表，可选是否包含仲裁者，结果按角色排序并映射为输出模型。 |
| findOneByJobRole | JobMemberMySqlModel | 方法根据业务ID、职位角色和成员ID查询JobMemberMySqlModel记录，返回匹配结果或null。 |
| findIdByMemberInfo | JobMemberMySqlModel | 方法通过SQL查询根据jobId、角色和memberId查找job_member表的id，若存在则返回对应实体，否则返回null。 |
| list | List<JobMemberOutputModel> | 这是一个Java方法，根据jobId列出JobMemberOutputModel对象列表，默认包含所有成员。 |
| findListByJobId | List<JobMemberMySqlModel> | 根据jobId查询JobMemberMySqlModel列表，使用equal条件构建查询并返回结果。 |
| isLocalJob | boolean | 检查任务是否为本地任务：通过jobId和当前用户ID查询数据库，排除仲裁者角色，若记录数大于1则返回true。 |




