# 基础信息

|      |      |
|------|------|
| 名称 | PredictStatisticsRepository |
| 编码语言 | .java |
| 代码路径 | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/database/repository/PredictStatisticsRepository.java |
| 包名 | com.welab.wefe.serving.service.database.repository |
| 依赖项 | ['com.welab.wefe.serving.service.database.entity.PredictStatisticsMySqlModel', 'com.welab.wefe.serving.service.database.repository.base.BaseRepository', 'org.springframework.data.jpa.repository.Query', 'org.springframework.data.repository.query.Param', 'org.springframework.stereotype.Repository', 'java.util.List'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| PredictStatisticsRepository | interface |  |



## 类 PredictStatisticsRepository

|      |      |
|------|------|
| 访问范围 | @Repository;public |
| 类型 | interface |
| 名称 | PredictStatisticsRepository |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| findByModelIdAndMemberId | PredictStatisticsMySqlModel |  |
| getMemberId | List<String> |  |
| findByHour | List<PredictStatisticsMySqlModel> |  |
| findByDay | List<PredictStatisticsMySqlModel> |  |
| getModelId | List<String> |  |
| findByMonth | List<PredictStatisticsMySqlModel> |  |
| findByMinute | List<PredictStatisticsMySqlModel> |  |




