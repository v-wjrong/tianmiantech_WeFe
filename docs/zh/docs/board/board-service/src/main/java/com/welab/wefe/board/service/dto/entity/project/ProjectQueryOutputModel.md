# 基础信息

|      |      |
|------|------|
| 名称 | ProjectQueryOutputModel |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/dto/entity/project/ProjectQueryOutputModel.java |
| 包名 | com.welab.wefe.board.service.dto.entity.project |
| 依赖项 | ['com.welab.wefe.board.service.dto.entity.AbstractOutputModel', 'com.welab.wefe.board.service.service.CacheObjects', 'com.welab.wefe.common.fieldvalidate.annotation.Check', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.wefe.enums.AuditStatus', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'com.welab.wefe.common.wefe.enums.ProjectType', 'java.util.Date', 'java.util.List'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| ProjectQueryOutputModel | class |  |



## 类 ProjectQueryOutputModel

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | ProjectQueryOutputModel |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| needMeAuditDataSetCount | int |  |
| exitedTime | Date |  |
| promoter | String |  |
| progress | Integer |  |
| projectDesc | String |  |
| finishTime | Date |  |
| myRole | JobMemberRole |  |
| closed = false | boolean |  |
| projectId | String |  |
| memberList | List<ProjectMemberOutputModel> |  |
| exitedBy | String |  |
| top | boolean |  |
| progressUpdatedTime | Date |  |
| message | String |  |
| memberId | String |  |
| flowStatusStatistics | JObject |  |
| auditStatus | AuditStatus |  |
| startTime | Date |  |
| statusUpdatedTime | Date |  |
| closedBy | String |  |
| promoterName | String |  |
| name | String |  |
| closedTime | Date |  |
| projectType | ProjectType |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| setMemberId | void |  |
| getPromoter | String |  |
| setExitedTime | void |  |
| setExitedBy | void |  |
| getClosedBy | String |  |
| getProjectId | String |  |
| setMessage | void |  |
| getAuditStatus | AuditStatus |  |
| getProjectDesc | String |  |
| isClosed | boolean |  |
| getProgress | Integer |  |
| getName | String |  |
| getCloseOperatorNickname | String |  |
| getMyRole | JobMemberRole |  |
| setFinishTime | void |  |
| getProgressUpdatedTime | Date |  |
| setStatusUpdatedTime | void |  |
| setPromoterName | void |  |
| setMyRole | void |  |
| setProgress | void |  |
| getFlowStatusStatistics | JObject |  |
| setName | void |  |
| setProjectDesc | void |  |
| setFlowStatusStatistics | void |  |
| getMemberList | List<ProjectMemberOutputModel> |  |
| getExitOperatorNickname | String |  |
| setPromoter | void |  |
| getMemberId | String |  |
| setProgressUpdatedTime | void |  |
| setClosed | void |  |
| getPromoterName | String |  |
| getExitedTime | Date |  |
| getExitedBy | String |  |
| setProjectId | void |  |
| getFinishTime | Date |  |
| getStartTime | Date |  |
| getStatusUpdatedTime | Date |  |
| setAuditStatus | void |  |
| setMemberList | void |  |
| setStartTime | void |  |
| getMessage | String |  |
| setClosedBy | void |  |
| getClosedTime | Date |  |
| setClosedTime | void |  |
| getNeedMeAuditDataSetCount | int |  |
| setNeedMeAuditDataSetCount | void |  |
| getProjectType | ProjectType |  |
| setProjectType | void |  |
| isTop | boolean |  |
| setTop | void |  |




