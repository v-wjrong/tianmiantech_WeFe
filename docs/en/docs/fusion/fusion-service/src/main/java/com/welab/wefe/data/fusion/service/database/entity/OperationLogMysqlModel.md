# Basic Information

|      |      |
|------|------|
| Name | OperationLogMysqlModel |
| Language | .java |
| Code Path | WeFe/fusion/fusion-service/src/main/java/com/welab/wefe/data/fusion/service/database/entity/OperationLogMysqlModel.java |
| Package Name | com.welab.wefe.data.fusion.service.database.entity |
| Dependencies | ['com.welab.wefe.common.web.delegate.api_log.ApiCallerType', 'javax.persistence.Entity', 'java.util.Date'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| OperationLogMysqlModel | class |  |



## Class OperationLogMysqlModel

|      |      |
|------|------|
| Access Modifier | @Entity(name = "operator_log");public |
| Type | class |
| Name | OperationLogMysqlModel |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
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

### Method List

| Name  | Type  | Description |
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




