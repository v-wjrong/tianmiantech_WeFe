# Basic Information

|      |      |
|------|------|
| Name | OperationLog |
| Language | .java |
| Code Path | WeFe/common/java/common-data-mongodb/src/main/java/com/welab/wefe/common/data/mongodb/entity/common/OperationLog.java |
| Package Name | com.welab.wefe.common.data.mongodb.entity.common |
| Dependencies | ['com.welab.wefe.common.data.mongodb.constant.MongodbTable', 'com.welab.wefe.common.data.mongodb.entity.base.AbstractNormalMongoModel', 'org.springframework.data.mongodb.core.mapping.Document', 'java.util.Date'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| OperationLog | class |  |



## Class OperationLog

|      |      |
|------|------|
| Access Modifier | @Document(collection = MongodbTable.Common.OPERATION_LOG);;public |
| Type | class |
| Name | OperationLog |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| callerName | String |  |
| requestData | String |  |
| responseMessage | String |  |
| responseData | String |  |
| requestTime | Date |  |
| spend | long |  |
| responseCode | int |  |
| callerIp | String |  |
| callerType | String |  |
| apiName | String |  |
| callerId | String |  |
| responseTime | Date |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getSpend | long |  |
| getResponseTime | Date |  |
| setSpend | void |  |
| setRequestData | void |  |
| getCallerId | String |  |
| setCallerId | void |  |
| getCallerIp | String |  |
| setRequestTime | void |  |
| setResponseTime | void |  |
| getResponseCode | int |  |
| getResponseMessage | String |  |
| setApiName | void |  |
| setCallerName | void |  |
| getCallerName | String |  |
| setResponseCode | void |  |
| getCallerType | String |  |
| getRequestData | String |  |
| setResponseMessage | void |  |
| setResponseData | void |  |
| setCallerType | void |  |
| getRequestTime | Date |  |
| getApiName | String |  |
| getResponseData | String |  |
| setCallerIp | void |  |




