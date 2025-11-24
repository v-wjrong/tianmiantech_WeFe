# 基础信息

|      |      |
|------|------|
| 名称 | OperationLogMysqlModel |
| 编码语言 | .java |
| 代码路径 | WeFe/fusion/fusion-service/src/main/java/com/welab/wefe/data/fusion/service/database/entity/OperationLogMysqlModel.java |
| 包名 | com.welab.wefe.data.fusion.service.database.entity |
| 依赖项 | ['com.welab.wefe.common.web.delegate.api_log.ApiCallerType', 'javax.persistence.Entity', 'java.util.Date'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| OperationLogMysqlModel | class |  |



## 类 OperationLogMysqlModel

|      |      |
|------|------|
| 访问范围 | @Entity(name = "operator_log");public |
| 类型 | class |
| 名称 | OperationLogMysqlModel |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| apiName | String |  |
| responseData | String |  |
| responseCode | int |  |
| callerType = ApiCallerType.User | ApiCallerType |  |
| responseMessage | String |  |
| callerIp | String |  |
| responseTime | Date |  |
| requestData | String |  |
| callerName | String |  |
| requestTime | Date |  |
| callerId | String |  |
| spend | long |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getRequestTime | Date |  |
| getRequestData | String |  |
| setCallerId | void |  |
| getResponseData | String |  |
| setCallerType | void |  |
| setCallerIp | void |  |
| getResponseMessage | String |  |
| setResponseTime | void |  |
| setRequestTime | void |  |
| setRequestData | void |  |
| getApiName | String |  |
| setSpend | void |  |
| setResponseMessage | void |  |
| getCallerType | ApiCallerType |  |
| setApiName | void |  |
| getResponseTime | Date |  |
| setResponseCode | void |  |
| getCallerName | String |  |
| getSpend | long |  |
| setCallerName | void |  |
| setResponseData | void |  |
| getCallerIp | String |  |
| getResponseCode | int |  |
| getCallerId | String |  |




