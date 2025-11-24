# Basic Information

|      |      |
|------|------|
| Name | PredictStatisticsRepository |
| Language | .java |
| Code Path | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/database/repository/PredictStatisticsRepository.java |
| Package Name | com.welab.wefe.serving.service.database.repository |
| Dependencies | ['com.welab.wefe.serving.service.database.entity.PredictStatisticsMySqlModel', 'com.welab.wefe.serving.service.database.repository.base.BaseRepository', 'org.springframework.data.jpa.repository.Query', 'org.springframework.data.repository.query.Param', 'org.springframework.stereotype.Repository', 'java.util.List'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| PredictStatisticsRepository | interface |  |



## Class PredictStatisticsRepository

|      |      |
|------|------|
| Access Modifier | @Repository;public |
| Type | interface |
| Name | PredictStatisticsRepository |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| findByModelIdAndMemberId | PredictStatisticsMySqlModel |  |
| getMemberId | List<String> |  |
| findByHour | List<PredictStatisticsMySqlModel> |  |
| findByDay | List<PredictStatisticsMySqlModel> |  |
| getModelId | List<String> |  |
| findByMonth | List<PredictStatisticsMySqlModel> |  |
| findByMinute | List<PredictStatisticsMySqlModel> |  |




