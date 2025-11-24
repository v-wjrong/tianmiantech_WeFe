# Basic Information

|      |      |
|------|------|
| Name | ProjectMySqlModel |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/database/entity/job/ProjectMySqlModel.java |
| Package Name | com.welab.wefe.board.service.database.entity.job |
| Dependencies | ['com.welab.wefe.board.service.database.entity.base.AbstractBaseMySqlModel', 'com.welab.wefe.common.wefe.enums.AuditStatus', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'com.welab.wefe.common.wefe.enums.ProjectType', 'javax.persistence.Entity', 'javax.persistence.EnumType', 'javax.persistence.Enumerated', 'java.util.Date'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| ProjectMySqlModel | class |  |



## Class ProjectMySqlModel

|      |      |
|------|------|
| Access Modifier | @Entity(name = "project");public |
| Type | class |
| Name | ProjectMySqlModel |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| name | String |  |
| exitedBy | String |  |
| deleted | boolean |  |
| message | String |  |
| sortNum | int |  |
| progress | Integer |  |
| finishTime | Date |  |
| auditStatusFromMyself | AuditStatus |  |
| closed = false | boolean |  |
| top | boolean |  |
| auditStatusFromOthers | AuditStatus |  |
| auditComment | String |  |
| myRole | JobMemberRole |  |
| exited = false | boolean |  |
| statusUpdatedTime | Date |  |
| progressUpdatedTime | Date |  |
| flowStatusStatistics | String |  |
| auditStatus | AuditStatus |  |
| exitedTime | Date |  |
| projectId | String |  |
| startTime | Date |  |
| closedTime | Date |  |
| serialVersionUID = -2632889286058354328L | long |  |
| projectDesc | String |  |
| memberId | String |  |
| projectType | ProjectType |  |
| closedBy | String |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| setAuditComment | void |  |
| getStatusUpdatedTime | Date |  |
| setDeleted | void |  |
| getAuditComment | String |  |
| getFlowStatusStatistics | String |  |
| getExitedTime | Date |  |
| setAuditStatusFromOthers | void |  |
| getAuditStatusFromOthers | AuditStatus |  |
| getProjectId | String |  |
| setTop | void |  |
| setExited | void |  |
| isTop | boolean |  |
| getAuditStatusFromMyself | AuditStatus |  |
| setMemberId | void |  |
| setExitedTime | void |  |
| getProjectType | ProjectType |  |
| getMemberId | String |  |
| isDeleted | boolean |  |
| setClosedTime | void |  |
| getAuditStatus | AuditStatus |  |
| setProjectId | void |  |
| setMessage | void |  |
| setAuditStatusFromMyself | void |  |
| setClosedBy | void |  |
| setProjectType | void |  |
| setProgressUpdatedTime | void |  |
| setProjectDesc | void |  |
| setMyRole | void |  |
| getClosedBy | String |  |
| getProgressUpdatedTime | Date |  |
| getName | String |  |
| getProgress | Integer |  |
| setName | void |  |
| getFinishTime | Date |  |
| getProjectDesc | String |  |
| getExitedBy | String |  |
| setFlowStatusStatistics | void |  |
| setStartTime | void |  |
| setProgress | void |  |
| getStartTime | Date |  |
| setExitedBy | void |  |
| setClosed | void |  |
| setAuditStatus | void |  |
| setStatusUpdatedTime | void |  |
| isClosed | boolean |  |
| setFinishTime | void |  |
| getSortNum | int |  |
| setSortNum | void |  |
| getClosedTime | Date |  |
| getMyRole | JobMemberRole |  |
| getMessage | String |  |
| isExited | boolean |  |




