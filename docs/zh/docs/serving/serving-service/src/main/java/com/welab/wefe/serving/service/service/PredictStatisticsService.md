# 基础信息

|      |      |
|------|------|
| 名称 | PredictStatisticsService |
| 编码语言 | .java |
| 代码路径 | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/service/PredictStatisticsService.java |
| 包名 | com.welab.wefe.serving.service.service |
| 依赖项 | ['com.alibaba.fastjson.util.TypeUtils', 'com.google.common.collect.Lists', 'com.welab.wefe.common.data.mysql.Where', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.DateUtil', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.web.util.ModelMapper', 'com.welab.wefe.serving.sdk.model.BaseModel', 'com.welab.wefe.serving.service.api.logger.StatisticsApi', 'com.welab.wefe.serving.service.database.entity.PredictStatisticsMySqlModel', 'com.welab.wefe.serving.service.database.repository.PredictStatisticsRepository', 'com.welab.wefe.serving.service.manager.ModelManager', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.data.jpa.domain.Specification', 'org.springframework.stereotype.Service', 'org.springframework.transaction.annotation.Transactional', 'java.util.Date', 'java.util.LinkedHashMap', 'java.util.List', 'java.util.Map', 'java.util.stream.Collectors'] |
| 概述说明 | PredictStatisticsService类提供预测统计功能，支持按时间区间查询日志，统计成功/失败次数，并支持按月、日、小时、分钟分页查询。核心方法包括初始化时间间隔、插入统计记录和计数日志。 |

# 说明

PredictStatisticsService是一个统计预测日志的服务类，主要功能包括按时间区间查询日志、插入统计记录、统计成功/失败日志数量、条件查询单条记录及分页查询。服务根据modelId和memberId的不同组合情况处理数据，支持按月、日、小时、分钟等不同时间粒度统计。统计时自动计算时间间隔，默认处理最近10分钟数据，也可自定义起止时间。分页查询结果会补充模型算法类型等附加信息。所有数据库操作通过PredictStatisticsRepository完成，插入操作具有事务回滚机制。

# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| PredictStatisticsService | class | PredictStatisticsService提供预测统计功能，支持按时间区间查询日志，统计成功/失败次数，并支持分页查询。可处理模型ID和成员ID的不同组合情况，自动初始化时间间隔。 |



## 类 PredictStatisticsService

|      |      |
|------|------|
| 访问范围 | @Service;public |
| 类型 | class |
| 名称 | PredictStatisticsService |
| 说明 | PredictStatisticsService提供预测统计功能，支持按时间区间查询日志，统计成功/失败次数，并支持分页查询。可处理模型ID和成员ID的不同组合情况，自动初始化时间间隔。 |


### UML类图

```mermaid
classDiagram
    class PredictStatisticsService {
        -Logger log
        -PredictStatisticsRepository predictStatisticsRepository
        +statisticsLog(String modelId, String memberId, String startDate, String endDate)
        -insertPredictStatistics(String modelId, String memberId, Map~String, String~ minuteIntervalMap)
        +countLog(String startTime, String endTime, String memberId, String modelId, boolean result) int
        +getOneByCondition(String modelId, String memberId, String minuteStr) PredictStatisticsMySqlModel
        +query(StatisticsApi.Input input) List~StatisticsApi.Output~
        +initMinuteIntervalMap(boolean useDefault, Date startDate, Date endDate) Map~String, String~
    }

    class PredictStatisticsRepository {
        <<Interface>>
        +getModelId() List~String~
        +getMemberId() List~String~
        +save(PredictStatisticsMySqlModel model)
        +query(String sql) List
        +findOne(Specification~PredictStatisticsMySqlModel~ where) Optional~PredictStatisticsMySqlModel~
        +findByMonth(String modelId, String memberId, String startMonth, String endMonth) List~PredictStatisticsMySqlModel~
        +findByDay(String modelId, String memberId, String startDay, String endDay) List~PredictStatisticsMySqlModel~
        +findByHour(String modelId, String memberId, String startHour, String endHour) List~PredictStatisticsMySqlModel~
        +findByMinute(String modelId, String memberId, String startMinute, String endMinute) List~PredictStatisticsMySqlModel~
    }

    class PredictStatisticsMySqlModel {
        +String memberId
        +String modelId
        +String dateFields
        +String minute
        +int success
        +int fail
        +int total
    }

    class StatisticsApi {
        class Input {
            +String modelId
            +String memberId
            +String dateType
            +int interval
        }
        class Output {
            +String modelId
            +String algorithm
            +String flType
            +String myRole
        }
    }

    PredictStatisticsService --> PredictStatisticsRepository : 依赖
    PredictStatisticsService --> PredictStatisticsMySqlModel : 操作
    PredictStatisticsService --> StatisticsApi : 使用
    PredictStatisticsRepository --> PredictStatisticsMySqlModel : 操作
```

该图展示了预测统计服务的核心类结构。PredictStatisticsService作为主服务类，通过PredictStatisticsRepository接口与数据库交互，操作PredictStatisticsMySqlModel实体类。服务提供日志统计、数据查询等功能，支持不同时间粒度（分钟/小时/天/月）的统计分析。StatisticsApi定义了输入输出数据结构，整个系统采用分层架构，通过依赖注入实现松耦合。


### 内部方法调用关系图

```mermaid
graph TD
    A["PredictStatisticsService"]
    B["statisticsLog方法"]
    C["insertPredictStatistics方法"]
    D["countLog方法"]
    E["getOneByCondition方法"]
    F["query方法"]
    G["initMinuteIntervalMap方法"]
    H["PredictStatisticsRepository"]
    I["ModelMapper"]
    J["ModelManager"]

    A --> B
    B -->|"StringUtil.isNotEmpty(startDate) && StringUtil.isNotEmpty(endDate)"| G
    B -->|else| G
    B -->|"StringUtil.isNotEmpty(memberId) && StringUtil.isEmpty(modelId)"| H
    B -->|"StringUtil.isEmpty(memberId) && StringUtil.isNotEmpty(modelId)"| H
    B -->|"StringUtil.isEmpty(memberId) && StringUtil.isEmpty(modelId)"| H
    B -->|else| C
    C --> D
    C --> E
    C --> H
    F --> H
    F --> I
    F --> J
    G -->|"useDefault=true"| "默认10分钟间隔"
    G -->|"useDefault=false"| "计算startDate-endDate间隔"
```

这段代码是PredictStatisticsService类的实现，主要用于预测统计数据的处理和查询。核心功能包括：1) 根据时间区间统计日志；2) 插入统计记录；3) 计算成功/失败日志数量；4) 条件查询单条记录；5) 分页查询统计数据；6) 初始化分钟间隔映射。流程图展示了各方法间的调用关系，其中statisticsLog作为入口方法，根据参数不同调用不同分支逻辑，最终通过insertPredictStatistics完成数据持久化。查询功能query则根据日期类型调用不同Repository方法，并映射结果到输出对象。

### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| log = LoggerFactory.getLogger(PredictStatisticsService.class) | Logger | 类PredictStatisticsService中定义了一个私有日志记录器log，用于记录日志信息。 |
| predictStatisticsRepository | PredictStatisticsRepository | 自动注入PredictStatisticsRepository实例。 |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| statisticsLog | void | 方法统计日志，根据modelId和memberId条件处理数据：无日期时初始化空时间间隔，否则按起止日期生成；根据ID组合情况调用insertPredictStatistics插入统计结果。 |
| countLog | int | 方法统计预测日志数量，根据时间、用户ID、模型ID和结果条件查询数据库并返回计数。 |
| insertPredictStatistics | void | 私有事务方法，按分钟统计模型预测成功与失败次数并入库，忽略已存在记录。 |
| getOneByCondition | PredictStatisticsMySqlModel | 根据条件查询预测统计记录，返回匹配的第一条数据或null。 |
| query | List<StatisticsApi.Output> | 方法根据输入日期类型查询预测统计数据，按不同时间粒度（月、日、小时、分钟）从数据库获取数据，转换为输出格式并补充模型信息后返回列表。 |
| initMinuteIntervalMap | Map<String, String> | 静态方法initMinuteIntervalMap生成时间间隔映射。默认生成近10分钟间隔，若指定起止日期则计算实际分钟数。返回按分钟划分的时间段键值对。 |




