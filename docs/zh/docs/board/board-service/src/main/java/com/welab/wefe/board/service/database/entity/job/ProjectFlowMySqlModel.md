# 基础信息

|      |      |
|------|------|
| 名称 | ProjectFlowMySqlModel |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/database/entity/job/ProjectFlowMySqlModel.java |
| 包名 | com.welab.wefe.board.service.database.entity.job |
| 依赖项 | ['com.welab.wefe.board.service.database.entity.base.AbstractBaseMySqlModel', 'com.welab.wefe.common.wefe.enums.DeepLearningJobType', 'com.welab.wefe.common.wefe.enums.FederatedLearningType', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'com.welab.wefe.common.wefe.enums.ProjectFlowStatus', 'javax.persistence.Entity', 'javax.persistence.EnumType', 'javax.persistence.Enumerated', 'java.util.Date'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| ProjectFlowMySqlModel | class |  |



## 类 ProjectFlowMySqlModel

|      |      |
|------|------|
| 访问范围 | @Entity(name = "project_flow");public |
| 类型 | class |
| 名称 | ProjectFlowMySqlModel |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
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

### 方法列表

| 名称  | 类型  | 说明 |
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




