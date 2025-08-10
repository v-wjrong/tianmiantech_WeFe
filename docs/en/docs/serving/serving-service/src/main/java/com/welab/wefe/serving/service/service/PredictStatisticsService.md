# Basic Information

|      |      |
|------|------|
| Name | PredictStatisticsService |
| Language | .java |
| Code Path | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/service/PredictStatisticsService.java |
| Package Name | com.welab.wefe.serving.service.service |
| Dependencies | ['com.alibaba.fastjson.util.TypeUtils', 'com.google.common.collect.Lists', 'com.welab.wefe.common.data.mysql.Where', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.DateUtil', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.web.util.ModelMapper', 'com.welab.wefe.serving.sdk.model.BaseModel', 'com.welab.wefe.serving.service.api.logger.StatisticsApi', 'com.welab.wefe.serving.service.database.entity.PredictStatisticsMySqlModel', 'com.welab.wefe.serving.service.database.repository.PredictStatisticsRepository', 'com.welab.wefe.serving.service.manager.ModelManager', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.data.jpa.domain.Specification', 'org.springframework.stereotype.Service', 'org.springframework.transaction.annotation.Transactional', 'java.util.Date', 'java.util.LinkedHashMap', 'java.util.List', 'java.util.Map', 'java.util.stream.Collectors'] |
| Brief Description | The `PredictStatisticsService` class provides predictive statistics functionality, supporting log queries by time intervals, counting success/failure instances, and enabling paginated queries by month, day, hour, or minute. Core methods include initializing time intervals, inserting statistical records, and counting logs. |

# Description

PredictStatisticsService is a service class for statistical prediction logging, with main functionalities including querying logs by time intervals, inserting statistical records, counting the number of successful/failed logs, conditional querying of single records, and paginated queries. The service processes data based on different combinations of modelId and memberId, supporting statistical aggregation by various time granularities such as month, day, hour, and minute. It automatically calculates time intervals during statistics, defaulting to processing the most recent 10 minutes of data while also allowing custom start and end times. Paginated query results are supplemented with additional information such as model algorithm types. All database operations are performed through PredictStatisticsRepository, with insert operations featuring a transaction rollback mechanism.

# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| PredictStatisticsService | class | The PredictStatisticsService provides predictive statistics functionality, supporting log queries by time intervals, counting success/failure instances, and enabling paginated queries. It can handle various combinations of model IDs and member IDs, automatically initializing time intervals. |



## Class PredictStatisticsService

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | PredictStatisticsService |
| Description | The PredictStatisticsService provides predictive statistics functionality, supporting log queries by time intervals, counting success/failure instances, and enabling paginated queries. It can handle various combinations of model IDs and member IDs, automatically initializing time intervals. |


### UML Class Diagram

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

    PredictStatisticsService --> PredictStatisticsRepository : Dependency
    PredictStatisticsService --> PredictStatisticsMySqlModel : Operates
    PredictStatisticsService --> StatisticsApi : Uses
    PredictStatisticsRepository --> PredictStatisticsMySqlModel : Operates
```

This diagram illustrates the core class structure of the prediction statistics service. The PredictStatisticsService acts as the main service class, interacting with the database through the PredictStatisticsRepository interface to manipulate the PredictStatisticsMySqlModel entity class. The service provides functionalities such as log statistics and data querying, supporting statistical analysis at different time granularities (minute/hour/day/month). The StatisticsApi defines the input and output data structures. The entire system adopts a layered architecture, achieving loose coupling through dependency injection.


### Internal Method Call Graph

```mermaid
graph TD
    A["PredictStatisticsService"]
    B["statisticsLog Method"]
    C["insertPredictStatistics Method"]
    D["countLog Method"]
    E["getOneByCondition Method"]
    F["query Method"]
    G["initMinuteIntervalMap Method"]
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
    G -->|"useDefault=true"| "Default 10-minute interval"
    G -->|"useDefault=false"| "Calculate startDate-endDate interval"
```

This code implements the PredictStatisticsService class, primarily handling prediction statistics data processing and queries. Core functionalities include: 1) Log statistics by time range; 2) Insert statistical records; 3) Count success/failure logs; 4) Conditional single-record queries; 5) Paginated statistics queries; 6) Initialize minute interval mapping. The flowchart illustrates method call relationships, where statisticsLog serves as the entry point, invoking different branch logic based on parameters, ultimately persisting data via insertPredictStatistics. The query function routes to different Repository methods based on date types and maps results to output objects.

### Field List

| Name  | Type  | Description |
|-------|-------|------|
| log = LoggerFactory.getLogger(PredictStatisticsService.class) | Logger | The class `PredictStatisticsService` defines a private logger `log` for recording log information. |
| predictStatisticsRepository | PredictStatisticsRepository | Automatically inject the PredictStatisticsRepository instance. |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| statisticsLog | void | Method statistics log: Processes data based on modelId and memberId conditions—initializes empty time intervals when no date is present, otherwise generates them according to the start and end dates. Inserts statistical results by calling insertPredictStatistics based on ID combinations. |
| countLog | int | Method for statistically predicting log count, querying the database based on time, user ID, model ID, and result conditions, and returning the count. |
| insertPredictStatistics | void | Private transaction method: Count the successful and failed predictions of the model per minute and store them in the database, ignoring existing records. |
| getOneByCondition | PredictStatisticsMySqlModel | Query the prediction statistics records based on conditions and return the first matching data or null. |
| query | List<StatisticsApi.Output> | The method queries forecast statistics based on the input date type, retrieves data from the database by different time granularities (month, day, hour, minute), converts it into the output format, and returns a list after supplementing model information. |
| initMinuteIntervalMap | Map<String, String> | The static method `initMinuteIntervalMap` generates a time interval mapping. By default, it produces intervals for the last 10 minutes. If start and end dates are specified, it calculates the actual minute count. It returns key-value pairs of time periods divided by minutes. |




