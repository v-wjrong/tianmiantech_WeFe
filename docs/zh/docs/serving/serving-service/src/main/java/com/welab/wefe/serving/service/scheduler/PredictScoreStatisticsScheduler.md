# 基础信息

|      |      |
|------|------|
| 名称 | PredictScoreStatisticsScheduler |
| 编码语言 | .java |
| 代码路径 | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/scheduler/PredictScoreStatisticsScheduler.java |
| 包名 | com.welab.wefe.serving.service.scheduler |
| 依赖项 | ['com.welab.wefe.serving.service.database.repository.TableModelRepository', 'com.welab.wefe.serving.service.service.ModelPredictScoreStatisticsService', 'com.welab.wefe.serving.service.service.TableModelService', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.scheduling.annotation.Scheduled', 'org.springframework.stereotype.Component', 'java.util.List'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| PredictScoreStatisticsScheduler | class |  |



## 类 PredictScoreStatisticsScheduler

|      |      |
|------|------|
| 访问范围 | @Component;public |
| 类型 | class |
| 名称 | PredictScoreStatisticsScheduler |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| statisticsService | ModelPredictScoreStatisticsService |  |
| tableModelService | TableModelService |  |
| logger = LoggerFactory.getLogger(PredictScoreStatisticsScheduler.class) | Logger |  |
| tableModelRepository | TableModelRepository |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| statistics | void |  |




