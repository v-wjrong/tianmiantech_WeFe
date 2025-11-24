# Basic Information

|      |      |
|------|------|
| Name | ModelPredictScoreStatisticsService |
| Language | .java |
| Code Path | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/service/ModelPredictScoreStatisticsService.java |
| Package Name | com.welab.wefe.serving.service.service |
| Dependencies | ['com.welab.wefe.common.CommonThreadPool', 'com.welab.wefe.common.data.mysql.Where', 'com.welab.wefe.common.util.DateUtil', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.serving.service.database.entity.ModelPredictScoreRecordMySqlModel', 'com.welab.wefe.serving.service.database.entity.ModelPredictScoreStatisticsMySqlModel', 'com.welab.wefe.serving.service.database.entity.TableModelMySqlModel', 'com.welab.wefe.serving.service.database.repository.ModelPredictScoreRecordRepository', 'com.welab.wefe.serving.service.database.repository.ModelPredictScoreStatisticsRepository', 'com.welab.wefe.serving.service.database.repository.TableModelRepository', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.data.jpa.domain.Specification', 'org.springframework.stereotype.Service', 'java.util.Date', 'java.util.List', 'java.util.stream.Collectors'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| ModelPredictScoreStatisticsService | class |  |



## Class ModelPredictScoreStatisticsService

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | ModelPredictScoreStatisticsService |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| recordRepository | ModelPredictScoreRecordRepository |  |
| LOG = LoggerFactory.getLogger(getClass()) | Logger |  |
| modelRepository | TableModelRepository |  |
| statisticsRepository | ModelPredictScoreStatisticsRepository |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| findBinningSplitPoint | List<Double> |  |
| increaseStatistics | void |  |
| refresh | void |  |
| increment | void |  |
| asyncIncrement | void |  |
| count | int |  |
| findByServiceIdAndDayAndBinning | ModelPredictScoreStatisticsMySqlModel |  |
| addRecord | void |  |




