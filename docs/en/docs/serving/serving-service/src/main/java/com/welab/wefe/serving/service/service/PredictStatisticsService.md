# Basic Information

|      |      |
|------|------|
| Name | PredictStatisticsService |
| Language | .java |
| Code Path | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/service/PredictStatisticsService.java |
| Package Name | com.welab.wefe.serving.service.service |
| Dependencies | ['com.alibaba.fastjson.util.TypeUtils', 'com.google.common.collect.Lists', 'com.welab.wefe.common.data.mysql.Where', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.DateUtil', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.web.util.ModelMapper', 'com.welab.wefe.serving.sdk.model.BaseModel', 'com.welab.wefe.serving.service.api.logger.StatisticsApi', 'com.welab.wefe.serving.service.database.entity.PredictStatisticsMySqlModel', 'com.welab.wefe.serving.service.database.repository.PredictStatisticsRepository', 'com.welab.wefe.serving.service.manager.ModelManager', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.data.jpa.domain.Specification', 'org.springframework.stereotype.Service', 'org.springframework.transaction.annotation.Transactional', 'java.util.Date', 'java.util.LinkedHashMap', 'java.util.List', 'java.util.Map', 'java.util.stream.Collectors'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| PredictStatisticsService | class |  |



## Class PredictStatisticsService

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | PredictStatisticsService |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| predictStatisticsRepository | PredictStatisticsRepository |  |
| log = LoggerFactory.getLogger(PredictStatisticsService.class) | Logger |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| statisticsLog | void |  |
| insertPredictStatistics | void |  |
| countLog | int |  |
| getOneByCondition | PredictStatisticsMySqlModel |  |
| query | List<StatisticsApi.Output> |  |
| initMinuteIntervalMap | Map<String, String> |  |




