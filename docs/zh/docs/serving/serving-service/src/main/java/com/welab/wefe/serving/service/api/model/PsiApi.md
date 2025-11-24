# 基础信息

|      |      |
|------|------|
| 名称 | PsiApi |
| 编码语言 | .java |
| 代码路径 | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/api/model/PsiApi.java |
| 包名 | com.welab.wefe.serving.service.api.model |
| 依赖项 | ['com.welab.wefe.common.fieldvalidate.annotation.Check', 'com.welab.wefe.common.util.DateUtil', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.web.api.base.AbstractApi', 'com.welab.wefe.common.web.api.base.Api', 'com.welab.wefe.common.web.dto.AbstractApiInput', 'com.welab.wefe.common.web.dto.AbstractApiOutput', 'com.welab.wefe.common.web.dto.ApiResult', 'com.welab.wefe.serving.service.database.entity.StatisticsSumModel', 'com.welab.wefe.serving.service.database.entity.TableModelMySqlModel', 'com.welab.wefe.serving.service.database.repository.PredictScoreStatisticsRepository', 'com.welab.wefe.serving.service.database.repository.TableModelRepository', 'org.apache.commons.compress.utils.Lists', 'org.springframework.beans.factory.annotation.Autowired', 'java.math.BigDecimal', 'java.util', 'java.util.stream.Collectors'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| PsiApi | class |  |



## 类 PsiApi

|      |      |
|------|------|
| 访问范围 | @Api(path = "model/psi", name = "模型稳定性指标", desc = "模型稳定性指标");public |
| 类型 | class |
| 名称 | PsiApi |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| statisticsRepository | PredictScoreStatisticsRepository |  |
| tableModelRepository | TableModelRepository |  |

### 方法列表

| 名称  | 类型  | 说明 |
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




