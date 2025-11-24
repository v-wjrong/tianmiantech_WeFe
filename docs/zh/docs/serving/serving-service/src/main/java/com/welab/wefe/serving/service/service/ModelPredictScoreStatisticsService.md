# 基础信息

|      |      |
|------|------|
| 名称 | ModelPredictScoreStatisticsService |
| 编码语言 | .java |
| 代码路径 | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/service/ModelPredictScoreStatisticsService.java |
| 包名 | com.welab.wefe.serving.service.service |
| 依赖项 | ['com.welab.wefe.common.CommonThreadPool', 'com.welab.wefe.common.data.mysql.Where', 'com.welab.wefe.common.util.DateUtil', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.serving.service.database.entity.ModelPredictScoreRecordMySqlModel', 'com.welab.wefe.serving.service.database.entity.ModelPredictScoreStatisticsMySqlModel', 'com.welab.wefe.serving.service.database.entity.TableModelMySqlModel', 'com.welab.wefe.serving.service.database.repository.ModelPredictScoreRecordRepository', 'com.welab.wefe.serving.service.database.repository.ModelPredictScoreStatisticsRepository', 'com.welab.wefe.serving.service.database.repository.TableModelRepository', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.data.jpa.domain.Specification', 'org.springframework.stereotype.Service', 'java.util.Date', 'java.util.List', 'java.util.stream.Collectors'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| ModelPredictScoreStatisticsService | class |  |



## 类 ModelPredictScoreStatisticsService

|      |      |
|------|------|
| 访问范围 | @Service;public |
| 类型 | class |
| 名称 | ModelPredictScoreStatisticsService |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| recordRepository | ModelPredictScoreRecordRepository |  |
| LOG = LoggerFactory.getLogger(getClass()) | Logger |  |
| modelRepository | TableModelRepository |  |
| statisticsRepository | ModelPredictScoreStatisticsRepository |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| findBinningSplitPoint | List<Double> |  |
| increaseStatistics | void |  |
| refresh | void |  |
| increment | void |  |
| asyncIncrement | void |  |
| count | int |  |
| findByServiceIdAndDayAndBinning | ModelPredictScoreStatisticsMySqlModel |  |
| addRecord | void |  |




