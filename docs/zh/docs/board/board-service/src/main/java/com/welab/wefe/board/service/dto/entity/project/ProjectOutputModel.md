# 基础信息

|      |      |
|------|------|
| 名称 | ProjectOutputModel |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/dto/entity/project/ProjectOutputModel.java |
| 包名 | com.welab.wefe.board.service.dto.entity.project |
| 依赖项 | ['com.welab.wefe.board.service.dto.entity.AbstractOutputModel', 'com.welab.wefe.board.service.service.CacheObjects', 'com.welab.wefe.common.fieldvalidate.annotation.Check', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.wefe.enums.AuditStatus', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'com.welab.wefe.common.wefe.enums.ProjectType', 'java.util.Date', 'java.util.List'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| ProjectOutputModel | class |  |



## 类 ProjectOutputModel

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | ProjectOutputModel |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
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

### 方法列表

| 名称  | 类型  | 说明 |
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




