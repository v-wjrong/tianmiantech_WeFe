# Basic Information

|      |      |
|------|------|
| Name | FlowGraph |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/model/FlowGraph.java |
| Package Name | com.welab.wefe.board.service.model |
| Dependencies | ['com.welab.wefe.board.service.component.base.filter.OutputItemFilterFunction', 'com.welab.wefe.board.service.component.base.io.NodeOutputItem', 'com.welab.wefe.board.service.component.base.io.OutputItem', 'com.welab.wefe.board.service.database.entity.job.JobMemberMySqlModel', 'com.welab.wefe.board.service.database.entity.job.JobMySqlModel', 'com.welab.wefe.board.service.database.entity.job.ProjectFlowNodeMySqlModel', 'com.welab.wefe.board.service.exception.FlowNodeException', 'com.welab.wefe.board.service.service.CacheObjects', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.wefe.enums.ComponentType', 'com.welab.wefe.common.wefe.enums.FederatedLearningType', 'org.apache.commons.collections4.CollectionUtils', 'java.util.ArrayList', 'java.util.List', 'java.util.function.Function'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| FlowGraph | class |  |



## Class FlowGraph

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | FlowGraph |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| isChild | boolean |  |
| findAllNodesFromParent | List<FlowGraphNode> |  |
| findOneNodeFromParent | FlowGraphNode |  |
| findModelingNodeFromParent | FlowGraphNode |  |
| findNodeOutputFromParent | NodeOutputItem |  |
| findValidationDataSetFromParent | FlowGraphNode |  |
| findOneNodeFromParent | FlowGraphNode |  |
| findAllNodesFromParent | void |  |
| findModelingNodeFromParent | FlowGraphNode |  |
| getJobMemberIsMe | JobMemberMySqlModel |  |




