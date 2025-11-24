# Basic Information

|      |      |
|------|------|
| Name | OperationLogMysqlModel |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/database/entity/OperationLogMysqlModel.java |
| Package Name | com.welab.wefe.board.service.database.entity |
| Dependencies | ['com.welab.wefe.board.service.database.entity.base.AbstractMySqlModel', 'javax.persistence.Entity', 'java.util.Date'] |
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
| spend | long |  |
| token | String |  |
| operatorId | String |  |
| logInterface | String |  |
| logAction | String |  |
| requestIp | String |  |
| interfaceName | String |  |
| requestTime | Date |  |
| resultCode | int |  |
| resultMessage | String |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| setResultCode | void |  |
| setOperatorId | void |  |
| getToken | String |  |
| getLogAction | String |  |
| setInterfaceName | void |  |
| setLogAction | void |  |
| getRequestIp | String |  |
| setResultMessage | void |  |
| getResultMessage | String |  |
| getResultCode | int |  |
| setRequestIp | void |  |
| setLogInterface | void |  |
| getLogInterface | String |  |
| getRequestTime | Date |  |
| setToken | void |  |
| getOperatorId | String |  |
| getInterfaceName | String |  |
| setRequestTime | void |  |
| getSpend | long |  |
| setSpend | void |  |




