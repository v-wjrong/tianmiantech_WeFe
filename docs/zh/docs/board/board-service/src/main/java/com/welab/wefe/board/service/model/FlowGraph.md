# 基础信息

|      |      |
|------|------|
| 名称 | FlowGraph |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/model/FlowGraph.java |
| 包名 | com.welab.wefe.board.service.model |
| 依赖项 | ['com.welab.wefe.board.service.component.base.filter.OutputItemFilterFunction', 'com.welab.wefe.board.service.component.base.io.NodeOutputItem', 'com.welab.wefe.board.service.component.base.io.OutputItem', 'com.welab.wefe.board.service.database.entity.job.JobMemberMySqlModel', 'com.welab.wefe.board.service.database.entity.job.JobMySqlModel', 'com.welab.wefe.board.service.database.entity.job.ProjectFlowNodeMySqlModel', 'com.welab.wefe.board.service.exception.FlowNodeException', 'com.welab.wefe.board.service.service.CacheObjects', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.wefe.enums.ComponentType', 'com.welab.wefe.common.wefe.enums.FederatedLearningType', 'org.apache.commons.collections4.CollectionUtils', 'java.util.ArrayList', 'java.util.List', 'java.util.function.Function'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| FlowGraph | class |  |



## 类 FlowGraph

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | FlowGraph |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|

### 方法列表

| 名称  | 类型  | 说明 |
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




