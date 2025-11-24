# 基础信息

|      |      |
|------|------|
| 名称 | OperationLog |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-data-mongodb/src/main/java/com/welab/wefe/common/data/mongodb/entity/common/OperationLog.java |
| 包名 | com.welab.wefe.common.data.mongodb.entity.common |
| 依赖项 | ['com.welab.wefe.common.data.mongodb.constant.MongodbTable', 'com.welab.wefe.common.data.mongodb.entity.base.AbstractNormalMongoModel', 'org.springframework.data.mongodb.core.mapping.Document', 'java.util.Date'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| OperationLog | class |  |



## 类 OperationLog

|      |      |
|------|------|
| 访问范围 | @Document(collection = MongodbTable.Common.OPERATION_LOG);;public |
| 类型 | class |
| 名称 | OperationLog |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
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

### 方法列表

| 名称  | 类型  | 说明 |
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




