# Basic Information

|      |      |
|------|------|
| Name | ProjectFlowOutputModel |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/dto/entity/project/ProjectFlowOutputModel.java |
| Package Name | com.welab.wefe.board.service.dto.entity.project |
| Dependencies | ['com.alibaba.fastjson.JSON', 'com.alibaba.fastjson.JSONObject', 'com.welab.wefe.board.service.dto.entity.AbstractOutputModel', 'com.welab.wefe.board.service.service.CacheObjects', 'com.welab.wefe.common.fieldvalidate.annotation.Check', 'com.welab.wefe.common.wefe.enums.DeepLearningJobType', 'com.welab.wefe.common.wefe.enums.FederatedLearningType', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'com.welab.wefe.common.wefe.enums.ProjectFlowStatus', 'java.util.Date'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| ProjectFlowOutputModel | class |  |



## Class ProjectFlowOutputModel

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | ProjectFlowOutputModel |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| flowName | String |  |
| flowId | String |  |
| deleted | Boolean |  |
| federatedLearningType | FederatedLearningType |  |
| myRole | JobMemberRole |  |
| creatorMemberId | String |  |
| deepLearningJobType | DeepLearningJobType |  |
| projectModelingOutputModel | ProjectModelingOutputModel |  |
| graph | JSONObject |  |
| top | boolean |  |
| message | String |  |
| statusUpdatedTime | Date |  |
| flowStatus | ProjectFlowStatus |  |
| projectId | String |  |
| flowDesc | String |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| isTop | boolean |  |
| setTop | void |  |
| getCreatorMemberId | String |  |
| getMessage | String |  |
| setDeleted | void |  |
| setFlowName | void |  |
| setFlowStatus | void |  |
| setFlowId | void |  |
| getFlowDesc | String |  |
| setDeepLearningJobType | void |  |
| setStatusUpdatedTime | void |  |
| getFlowName | String |  |
| setCreatorMemberId | void |  |
| getProjectModelingOutputModel | ProjectModelingOutputModel |  |
| getFlowId | String |  |
| getProjectId | String |  |
| getMyRole | JobMemberRole |  |
| setProjectId | void |  |
| getFederatedLearningType | FederatedLearningType |  |
| getStatusUpdatedTime | Date |  |
| setProjectModelingOutputModel | void |  |
| setMyRole | void |  |
| setGraph | void |  |
| getFlowStatus | ProjectFlowStatus |  |
| getGraph | JSONObject |  |
| setFlowDesc | void |  |
| setMessage | void |  |
| getDeleted | Boolean |  |
| getDeepLearningJobType | DeepLearningJobType |  |
| setFederatedLearningType | void |  |
| getCreatorMemberName | String |  |




