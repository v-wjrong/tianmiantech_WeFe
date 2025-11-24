# 基础信息

|      |      |
|------|------|
| 名称 | OperationLogMysqlModel |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/database/entity/OperationLogMysqlModel.java |
| 包名 | com.welab.wefe.board.service.database.entity |
| 依赖项 | ['com.welab.wefe.board.service.database.entity.base.AbstractMySqlModel', 'javax.persistence.Entity', 'java.util.Date'] |
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

### 方法列表

| 名称  | 类型  | 说明 |
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




