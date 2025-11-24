# 基础信息

|      |      |
|------|------|
| 名称 | LogStatisticsScheduler |
| 编码语言 | .java |
| 代码路径 | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/scheduler/LogStatisticsScheduler.java |
| 包名 | com.welab.wefe.serving.service.scheduler |
| 依赖项 | ['com.welab.wefe.serving.service.service.PredictStatisticsService', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.scheduling.annotation.Scheduled', 'org.springframework.stereotype.Component'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| LogStatisticsScheduler | class |  |



## 类 LogStatisticsScheduler

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | LogStatisticsScheduler |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| logger = LoggerFactory.getLogger(LogStatisticsScheduler.class) | Logger |  |
| predictStatisticsService | PredictStatisticsService |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| logStatistics | void |  |




