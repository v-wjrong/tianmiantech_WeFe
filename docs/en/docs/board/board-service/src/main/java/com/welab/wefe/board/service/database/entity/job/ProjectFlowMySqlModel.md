# Basic Information

|      |      |
|------|------|
| Name | ProjectFlowMySqlModel |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/database/entity/job/ProjectFlowMySqlModel.java |
| Package Name | com.welab.wefe.board.service.database.entity.job |
| Dependencies | ['com.welab.wefe.board.service.database.entity.base.AbstractBaseMySqlModel', 'com.welab.wefe.common.wefe.enums.DeepLearningJobType', 'com.welab.wefe.common.wefe.enums.FederatedLearningType', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'com.welab.wefe.common.wefe.enums.ProjectFlowStatus', 'javax.persistence.Entity', 'javax.persistence.EnumType', 'javax.persistence.Enumerated', 'java.util.Date'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| ProjectFlowMySqlModel | class |  |



## Class ProjectFlowMySqlModel

|      |      |
|------|------|
| Access Modifier | @Entity(name = "project_flow");public |
| Type | class |
| Name | ProjectFlowMySqlModel |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| deepLearningJobType | DeepLearningJobType |  |
| creatorMemberId | String |  |
| deleted = false | boolean |  |
| graph | String |  |
| projectId | String |  |
| flowId | String |  |
| top | boolean |  |
| message | String |  |
| myRole | JobMemberRole |  |
| statusUpdatedTime | Date |  |
| flowStatus | ProjectFlowStatus |  |
| flowName | String |  |
| federatedLearningType | FederatedLearningType |  |
| flowDesc | String |  |
| serialVersionUID = -2604406277609318163L | long |  |
| sortNum | int |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| setFlowDesc | void |  |
| getFlowDesc | String |  |
| setFlowName | void |  |
| setDeleted | void |  |
| getDeepLearningJobType | DeepLearningJobType |  |
| setCreatorMemberId | void |  |
| setMyRole | void |  |
| getMessage | String |  |
| isTop | boolean |  |
| setMessage | void |  |
| setStatusUpdatedTime | void |  |
| getCreatorMemberId | String |  |
| setGraph | void |  |
| setDeepLearningJobType | void |  |
| setProjectId | void |  |
| getFederatedLearningType | FederatedLearningType |  |
| setFlowId | void |  |
| getProjectId | String |  |
| setTop | void |  |
| getMyRole | JobMemberRole |  |
| getDeleted | boolean |  |
| getStatusUpdatedTime | Date |  |
| getGraph | String |  |
| getFlowStatus | ProjectFlowStatus |  |
| getFlowName | String |  |
| getFlowId | String |  |
| setFlowStatus | void |  |
| setFederatedLearningType | void |  |
| getSortNum | int |  |
| setSortNum | void |  |




