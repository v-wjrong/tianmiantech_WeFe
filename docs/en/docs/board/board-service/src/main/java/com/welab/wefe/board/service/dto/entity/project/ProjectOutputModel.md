# Basic Information

|      |      |
|------|------|
| Name | ProjectOutputModel |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/dto/entity/project/ProjectOutputModel.java |
| Package Name | com.welab.wefe.board.service.dto.entity.project |
| Dependencies | ['com.welab.wefe.board.service.dto.entity.AbstractOutputModel', 'com.welab.wefe.board.service.service.CacheObjects', 'com.welab.wefe.common.fieldvalidate.annotation.Check', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.wefe.enums.AuditStatus', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'com.welab.wefe.common.wefe.enums.ProjectType', 'java.util.Date', 'java.util.List'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| ProjectOutputModel | class |  |



## Class ProjectOutputModel

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | ProjectOutputModel |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| auditStatus | AuditStatus |  |
| promoterList | List<ProjectDetailMemberOutputModel> |  |
| closedTime | Date |  |
| projectDesc | String |  |
| auditStatusFromMyself | AuditStatus |  |
| promoter | ProjectDetailMemberOutputModel |  |
| isCreator | boolean |  |
| myRole | JobMemberRole |  |
| auditStatusFromOthers | AuditStatus |  |
| flowStatusStatistics | JObject |  |
| exitedBy | String |  |
| closedBy | String |  |
| projectType | ProjectType |  |
| name | String |  |
| exitedTime | Date |  |
| closed = false | boolean |  |
| top | boolean |  |
| isExited | boolean |  |
| providerList | List<ProjectDetailMemberOutputModel> |  |
| message | String |  |
| projectId | String |  |
| memberId | String |  |
| auditComment | String |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getExitOperatorNickname | String |  |
| setFlowStatusStatistics | void |  |
| getPromoterList | List<ProjectDetailMemberOutputModel> |  |
| getFlowStatusStatistics | JObject |  |
| setClosedTime | void |  |
| getName | String |  |
| getExitedBy | String |  |
| getAuditStatus | AuditStatus |  |
| setPromoterList | void |  |
| getIsCreator | boolean |  |
| getIsExited | boolean |  |
| setIsExited | void |  |
| getProjectType | ProjectType |  |
| setProjectType | void |  |
| isTop | boolean |  |
| setTop | void |  |
| getMessage | String |  |
| setProjectDesc | void |  |
| setExitedBy | void |  |
| getAuditComment | String |  |
| getProjectDesc | String |  |
| setName | void |  |
| getAuditStatusFromOthers | AuditStatus |  |
| getProviderList | List<ProjectDetailMemberOutputModel> |  |
| setAuditComment | void |  |
| setAuditStatusFromMyself | void |  |
| setClosedBy | void |  |
| getExitedTime | Date |  |
| setMyRole | void |  |
| setPromoter | void |  |
| getMemberId | String |  |
| setAuditStatusFromOthers | void |  |
| setIsCreator | void |  |
| setAuditStatus | void |  |
| setMemberId | void |  |
| setClosed | void |  |
| getMyRole | JobMemberRole |  |
| getProjectId | String |  |
| getClosedTime | Date |  |
| setExitedTime | void |  |
| setProviderList | void |  |
| setMessage | void |  |
| setProjectId | void |  |
| getCloseOperatorNickname | String |  |
| isClosed | boolean |  |
| getClosedBy | String |  |
| getPromoter | ProjectDetailMemberOutputModel |  |
| getAuditStatusFromMyself | AuditStatus |  |




