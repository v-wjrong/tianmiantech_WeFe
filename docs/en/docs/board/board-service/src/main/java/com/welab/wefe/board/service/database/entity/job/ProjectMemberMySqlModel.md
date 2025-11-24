# Basic Information

|      |      |
|------|------|
| Name | ProjectMemberMySqlModel |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/database/entity/job/ProjectMemberMySqlModel.java |
| Package Name | com.welab.wefe.board.service.database.entity.job |
| Dependencies | ['com.welab.wefe.board.service.database.entity.base.AbstractBaseMySqlModel', 'com.welab.wefe.common.wefe.enums.AuditStatus', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'javax.persistence.Entity', 'javax.persistence.EnumType', 'javax.persistence.Enumerated'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| ProjectMemberMySqlModel | class |  |



## Class ProjectMemberMySqlModel

|      |      |
|------|------|
| Access Modifier | @Entity(name = "project_member");public |
| Type | class |
| Name | ProjectMemberMySqlModel |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| fromCreateProject | boolean |  |
| memberRole | JobMemberRole |  |
| exited = false | Boolean |  |
| auditStatus | AuditStatus |  |
| serialVersionUID = -2632889286058354328L | long |  |
| auditComment | String |  |
| auditStatusFromMyself | AuditStatus |  |
| memberId | String |  |
| projectId | String |  |
| inviterId | String |  |
| auditStatusFromOthers | AuditStatus |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getAuditStatusFromMyself | AuditStatus |  |
| getAuditStatusFromOthers | AuditStatus |  |
| setAuditStatusFromOthers | void |  |
| getAuditComment | String |  |
| setAuditComment | void |  |
| isExited | Boolean |  |
| setMemberRole | void |  |
| getMemberId | String |  |
| setExited | void |  |
| isFromCreateProject | boolean |  |
| getAuditStatus | AuditStatus |  |
| setInviterId | void |  |
| setAuditStatus | void |  |
| getProjectId | String |  |
| getMemberRole | JobMemberRole |  |
| setMemberId | void |  |
| setAuditStatusFromMyself | void |  |
| setFromCreateProject | void |  |
| getProjectRoleIndex | int |  |
| setProjectId | void |  |
| getInviterId | String |  |




