# Basic Information

|      |      |
|------|------|
| Name | PsiApi |
| Language | .java |
| Code Path | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/api/model/PsiApi.java |
| Package Name | com.welab.wefe.serving.service.api.model |
| Dependencies | ['com.welab.wefe.common.fieldvalidate.annotation.Check', 'com.welab.wefe.common.util.DateUtil', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.web.api.base.AbstractApi', 'com.welab.wefe.common.web.api.base.Api', 'com.welab.wefe.common.web.dto.AbstractApiInput', 'com.welab.wefe.common.web.dto.AbstractApiOutput', 'com.welab.wefe.common.web.dto.ApiResult', 'com.welab.wefe.serving.service.database.entity.StatisticsSumModel', 'com.welab.wefe.serving.service.database.entity.TableModelMySqlModel', 'com.welab.wefe.serving.service.database.repository.PredictScoreStatisticsRepository', 'com.welab.wefe.serving.service.database.repository.TableModelRepository', 'org.apache.commons.compress.utils.Lists', 'org.springframework.beans.factory.annotation.Autowired', 'java.math.BigDecimal', 'java.util', 'java.util.stream.Collectors'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| PsiApi | class |  |



## Class PsiApi

|      |      |
|------|------|
| Access Modifier | @Api(path = "model/psi", name = "模型稳定性指标", desc = "模型稳定性指标");public |
| Type | class |
| Name | PsiApi |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| statisticsRepository | PredictScoreStatisticsRepository |  |
| tableModelRepository | TableModelRepository |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| handle | ApiResult<Output> |  |
| extractYAxis | int |  |
| sum | int |  |
| extractActualDataByGroup | List<Object> |  |
| extractXAxis | String |  |
| formatDate | String |  |
| rate | double |  |
| sort | List<StatisticsSumModel> |  |
| psi | double |  |
| getBinningInfo | List<StatisticsSumModel> |  |
| subtract | double |  |
| main | void |  |
| psiList | List<List<Object>> |  |
| getDayList | List<DayModel> |  |
| extractExpectedData | List<List<Object>> |  |
| ln | double |  |
| extractActualData | List<List<Object>> |  |
| extractYAxis2 | double |  |
| extractXAxis2 | String |  |
| newScale | double |  |




