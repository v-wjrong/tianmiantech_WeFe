# Basic Information

|      |      |
|------|------|
| Name | ProjectFlowNodeMySqlModel |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/database/entity/job/ProjectFlowNodeMySqlModel.java |
| Package Name | com.welab.wefe.board.service.database.entity.job |
| Dependencies | ['com.welab.wefe.board.service.database.entity.base.AbstractBaseMySqlModel', 'com.welab.wefe.common.wefe.enums.ComponentType', 'javax.persistence.Entity', 'javax.persistence.EnumType', 'javax.persistence.Enumerated'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| ProjectFlowNodeMySqlModel | class |  |



## Class ProjectFlowNodeMySqlModel

|      |      |
|------|------|
| Access Modifier | @Entity(name = "project_flow_node");public |
| Type | class |
| Name | ProjectFlowNodeMySqlModel |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
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

### Method List

| Name  | Type  | Description |
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




