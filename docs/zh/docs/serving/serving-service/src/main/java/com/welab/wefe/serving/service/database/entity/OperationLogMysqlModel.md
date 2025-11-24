# 基础信息

|      |      |
|------|------|
| 名称 | OperationLogMysqlModel |
| 编码语言 | .java |
| 代码路径 | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/database/entity/OperationLogMysqlModel.java |
| 包名 | com.welab.wefe.serving.service.database.entity |
| 依赖项 | ['java.util.Date', 'javax.persistence.Column', 'javax.persistence.Entity'] |
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
| logInterface | String |  |
| requestIp | String |  |
| logAction | String |  |
| interfaceName | String |  |
| resultCode | int |  |
| token | String |  |
| resultMessage | String |  |
| spend | long |  |
| operatorId | String |  |
| serialVersionUID = 6979249624126197334L | long |  |
| requestTime | Date |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getLogAction | String |  |
| setRequestIp | void |  |
| setLogAction | void |  |
| getResultCode | int |  |
| setOperatorId | void |  |
| setResultMessage | void |  |
| getToken | String |  |
| getLogInterface | String |  |
| getInterfaceName | String |  |
| getResultMessage | String |  |
| setToken | void |  |
| setLogInterface | void |  |
| getOperatorId | String |  |
| setInterfaceName | void |  |
| getRequestIp | String |  |
| setResultCode | void |  |
| getRequestTime | Date |  |
| setRequestTime | void |  |
| getSpend | long |  |
| setSpend | void |  |




