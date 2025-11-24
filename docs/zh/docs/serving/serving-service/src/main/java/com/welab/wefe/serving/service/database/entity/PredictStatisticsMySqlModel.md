# 基础信息

|      |      |
|------|------|
| 名称 | PredictStatisticsMySqlModel |
| 编码语言 | .java |
| 代码路径 | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/database/entity/PredictStatisticsMySqlModel.java |
| 包名 | com.welab.wefe.serving.service.database.entity |
| 依赖项 | ['com.welab.wefe.common.util.DateUtil', 'javax.persistence', 'java.util.Date'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| PredictStatisticsMySqlModel | class |  |



## 类 PredictStatisticsMySqlModel

|      |      |
|------|------|
| 访问范围 | @Entity(name = "predict_statistics");public |
| 类型 | class |
| 名称 | PredictStatisticsMySqlModel |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| createdTime = new Date() | Date |  |
| id | int |  |
| fail | long |  |
| minute | String |  |
| hour | String |  |
| day | String |  |
| updatedTime | Date |  |
| total | long |  |
| success | long |  |
| modelId | String |  |
| memberId | String |  |
| month | String |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getMinute | String |  |
| getFail | long |  |
| getTotal | long |  |
| setMonth | void |  |
| setMinute | void |  |
| setHour | void |  |
| getHour | String |  |
| setMemberId | void |  |
| getCreatedTime | Date |  |
| setTotal | void |  |
| getMonth | String |  |
| setId | void |  |
| getId | int |  |
| setSuccess | void |  |
| setCreatedTime | void |  |
| getDay | String |  |
| setModelId | void |  |
| getModelId | String |  |
| setDay | void |  |
| getMemberId | String |  |
| getSuccess | long |  |
| getUpdatedTime | Date |  |
| setFail | void |  |
| setUpdatedTime | void |  |
| setDateFields | void |  |




