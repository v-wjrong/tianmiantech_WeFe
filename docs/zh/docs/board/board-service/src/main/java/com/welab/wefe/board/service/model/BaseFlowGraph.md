# 基础信息

|      |      |
|------|------|
| 名称 | BaseFlowGraph |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/model/BaseFlowGraph.java |
| 包名 | com.welab.wefe.board.service.model |
| 依赖项 | ['com.welab.wefe.board.service.component.Components', 'com.welab.wefe.board.service.component.base.AbstractComponent', 'com.welab.wefe.board.service.database.entity.job.JobMemberMySqlModel', 'com.welab.wefe.board.service.database.entity.job.JobMySqlModel', 'com.welab.wefe.board.service.database.entity.job.ProjectFlowNodeMySqlModel', 'com.welab.wefe.board.service.exception.FlowNodeException', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.web.util.ModelMapper', 'com.welab.wefe.common.wefe.enums.FederatedLearningType', 'org.apache.commons.collections4.CollectionUtils', 'java.util.ArrayList', 'java.util.Comparator', 'java.util.List', 'java.util.stream.Collectors'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| BaseFlowGraph | class |  |



## 类 BaseFlowGraph

|      |      |
|------|------|
| 访问范围 | public abstract |
| 类型 | class |
| 名称 | BaseFlowGraph |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| jobSteps = new ArrayList<>() | List<FlowGraphNode> |  |
| startNodes | List<FlowGraphNode> |  |
| job | JobMySqlModel |  |
| allNodes = new ArrayList<>() | List<FlowGraphNode> |  |
| lastJob | JobMySqlModel |  |
| members | List<JobMemberMySqlModel> |  |
| creatorMemberId | String |  |
| federatedLearningType | FederatedLearningType |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getStartNodes | List<FlowGraphNode> |  |
| setCreatorMemberId | void |  |
| findJobSteps | void |  |
| findOneById | FlowGraphNode |  |
| findParents | List<FlowGraphNode> |  |
| checkEndlessLoop | void |  |
| findChildren | List<FlowGraphNode> |  |
| getJobSteps | List<FlowGraphNode> |  |
| getLastJob | JobMySqlModel |  |
| recursiveDescent | boolean |  |
| sortJobSteps | void |  |
| getNode | FlowGraphNode |  |
| getAllJobSteps | List<FlowGraphNode> |  |
| getJob | JobMySqlModel |  |
| getMembers | List<JobMemberMySqlModel> |  |
| getFederatedLearningType | FederatedLearningType |  |
| getCreatorMemberId | String |  |




