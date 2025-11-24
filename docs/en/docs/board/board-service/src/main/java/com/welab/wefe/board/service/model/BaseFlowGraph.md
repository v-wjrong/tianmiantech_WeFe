# Basic Information

|      |      |
|------|------|
| Name | BaseFlowGraph |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/model/BaseFlowGraph.java |
| Package Name | com.welab.wefe.board.service.model |
| Dependencies | ['com.welab.wefe.board.service.component.Components', 'com.welab.wefe.board.service.component.base.AbstractComponent', 'com.welab.wefe.board.service.database.entity.job.JobMemberMySqlModel', 'com.welab.wefe.board.service.database.entity.job.JobMySqlModel', 'com.welab.wefe.board.service.database.entity.job.ProjectFlowNodeMySqlModel', 'com.welab.wefe.board.service.exception.FlowNodeException', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.web.util.ModelMapper', 'com.welab.wefe.common.wefe.enums.FederatedLearningType', 'org.apache.commons.collections4.CollectionUtils', 'java.util.ArrayList', 'java.util.Comparator', 'java.util.List', 'java.util.stream.Collectors'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| BaseFlowGraph | class |  |



## Class BaseFlowGraph

|      |      |
|------|------|
| Access Modifier | public abstract |
| Type | class |
| Name | BaseFlowGraph |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| jobSteps = new ArrayList<>() | List<FlowGraphNode> |  |
| startNodes | List<FlowGraphNode> |  |
| job | JobMySqlModel |  |
| allNodes = new ArrayList<>() | List<FlowGraphNode> |  |
| lastJob | JobMySqlModel |  |
| members | List<JobMemberMySqlModel> |  |
| creatorMemberId | String |  |
| federatedLearningType | FederatedLearningType |  |

### Method List

| Name  | Type  | Description |
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




