# 基础信息

|      |      |
|------|------|
| 名称 | ProjectFlowNodeMySqlModel |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/database/entity/job/ProjectFlowNodeMySqlModel.java |
| 包名 | com.welab.wefe.board.service.database.entity.job |
| 依赖项 | ['com.welab.wefe.board.service.database.entity.base.AbstractBaseMySqlModel', 'com.welab.wefe.common.wefe.enums.ComponentType', 'javax.persistence.Entity', 'javax.persistence.EnumType', 'javax.persistence.Enumerated'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| ProjectFlowNodeMySqlModel | class |  |



## 类 ProjectFlowNodeMySqlModel

|      |      |
|------|------|
| 访问范围 | @Entity(name = "project_flow_node");public |
| 类型 | class |
| 名称 | ProjectFlowNodeMySqlModel |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| paramsVersion = System.currentTimeMillis() | long |  |
| componentType | ComponentType |  |
| serialVersionUID = 2722275392448819712L | long |  |
| nodeId | String |  |
| startNode | boolean |  |
| params | String |  |
| projectId | String |  |
| parentNodeIdList | String |  |
| flowId | String |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getProjectId | String |  |
| setNodeId | void |  |
| setStartNode | void |  |
| setProjectId | void |  |
| getFlowId | String |  |
| isStartNode | boolean |  |
| setFlowId | void |  |
| getNodeId | String |  |
| getParams | String |  |
| setComponentType | void |  |
| getComponentType | ComponentType |  |
| setParams | void |  |
| getParentNodeIdList | String |  |
| setParentNodeIdList | void |  |
| getParamsVersion | long |  |
| setParamsVersion | void |  |




