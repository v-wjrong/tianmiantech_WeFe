# Basic Information

|      |      |
|------|------|
| Name | FlowGraphNode |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/model/FlowGraphNode.java |
| Package Name | com.welab.wefe.board.service.model |
| Dependencies | ['cn.hutool.core.collection.CollectionUtil', 'com.welab.wefe.board.service.component.Components', 'com.welab.wefe.board.service.component.base.AbstractComponent', 'com.welab.wefe.board.service.database.entity.job.JobMySqlModel', 'com.welab.wefe.board.service.database.entity.job.ProjectFlowNodeMySqlModel', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.fieldvalidate.AbstractCheckModel', 'com.welab.wefe.common.wefe.enums.ComponentType', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'org.apache.commons.lang3.StringUtils', 'java.util.ArrayList', 'java.util.List', 'java.util.stream.Collectors'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| FlowGraphNode | class |  |



## Class FlowGraphNode

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | FlowGraphNode |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| paramsModel | AbstractCheckModel |  |
| parents = new ArrayList<>() | List<FlowGraphNode> |  |
| taskName | String |  |
| position | Integer |  |
| children = new ArrayList<>() | List<FlowGraphNode> |  |
| hasCacheResult | Boolean |  |
| deep | Integer |  |
| leafNode = false | boolean |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getParents | List<FlowGraphNode> |  |
| getDeep | Integer |  |
| setDeep | void |  |
| setTaskName | void |  |
| getComponent | AbstractComponent<?> |  |
| getHasCacheResult | Boolean |  |
| createTaskName | String |  |
| createTaskId | String |  |
| createTaskId | String |  |
| createParentTaskIds | String |  |
| createTaskId | String |  |
| getPosition | Integer |  |
| setParents | void |  |
| createTaskId | String |  |
| getTaskName | String |  |
| getParamsModel | T |  |
| setHasCacheResult | void |  |
| setPosition | void |  |
| createParentTaskIds | String |  |
| getChildren | List<FlowGraphNode> |  |
| setChildren | void |  |
| isLeafNode | boolean |  |
| setLeafNode | void |  |




