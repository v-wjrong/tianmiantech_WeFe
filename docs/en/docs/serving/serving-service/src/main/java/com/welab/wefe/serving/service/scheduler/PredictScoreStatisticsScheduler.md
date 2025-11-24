# Basic Information

|      |      |
|------|------|
| Name | PredictScoreStatisticsScheduler |
| Language | .java |
| Code Path | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/scheduler/PredictScoreStatisticsScheduler.java |
| Package Name | com.welab.wefe.serving.service.scheduler |
| Dependencies | ['com.welab.wefe.serving.service.database.repository.TableModelRepository', 'com.welab.wefe.serving.service.service.ModelPredictScoreStatisticsService', 'com.welab.wefe.serving.service.service.TableModelService', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.scheduling.annotation.Scheduled', 'org.springframework.stereotype.Component', 'java.util.List'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| PredictScoreStatisticsScheduler | class |  |



## Class PredictScoreStatisticsScheduler

|      |      |
|------|------|
| Access Modifier | @Component;public |
| Type | class |
| Name | PredictScoreStatisticsScheduler |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| statisticsService | ModelPredictScoreStatisticsService |  |
| tableModelService | TableModelService |  |
| logger = LoggerFactory.getLogger(PredictScoreStatisticsScheduler.class) | Logger |  |
| tableModelRepository | TableModelRepository |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| statistics | void |  |




