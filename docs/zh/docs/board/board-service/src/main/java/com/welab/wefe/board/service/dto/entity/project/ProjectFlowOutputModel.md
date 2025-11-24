# 基础信息

|      |      |
|------|------|
| 名称 | ProjectFlowOutputModel |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/dto/entity/project/ProjectFlowOutputModel.java |
| 包名 | com.welab.wefe.board.service.dto.entity.project |
| 依赖项 | ['com.alibaba.fastjson.JSON', 'com.alibaba.fastjson.JSONObject', 'com.welab.wefe.board.service.dto.entity.AbstractOutputModel', 'com.welab.wefe.board.service.service.CacheObjects', 'com.welab.wefe.common.fieldvalidate.annotation.Check', 'com.welab.wefe.common.wefe.enums.DeepLearningJobType', 'com.welab.wefe.common.wefe.enums.FederatedLearningType', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'com.welab.wefe.common.wefe.enums.ProjectFlowStatus', 'java.util.Date'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| ProjectFlowOutputModel | class |  |



## 类 ProjectFlowOutputModel

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | ProjectFlowOutputModel |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
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

### 方法列表

| 名称  | 类型  | 说明 |
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




