# Basic Information

|      |      |
|------|------|
| Name | ProjectQueryOutputModel |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/dto/entity/project/ProjectQueryOutputModel.java |
| Package Name | com.welab.wefe.board.service.dto.entity.project |
| Dependencies | ['com.welab.wefe.board.service.dto.entity.AbstractOutputModel', 'com.welab.wefe.board.service.service.CacheObjects', 'com.welab.wefe.common.fieldvalidate.annotation.Check', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.wefe.enums.AuditStatus', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'com.welab.wefe.common.wefe.enums.ProjectType', 'java.util.Date', 'java.util.List'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| ProjectQueryOutputModel | class |  |



## Class ProjectQueryOutputModel

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | ProjectQueryOutputModel |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
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

### Method List

| Name  | Type  | Description |
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




