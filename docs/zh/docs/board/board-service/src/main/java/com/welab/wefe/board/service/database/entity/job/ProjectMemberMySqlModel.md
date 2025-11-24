# 基础信息

|      |      |
|------|------|
| 名称 | ProjectMemberMySqlModel |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/database/entity/job/ProjectMemberMySqlModel.java |
| 包名 | com.welab.wefe.board.service.database.entity.job |
| 依赖项 | ['com.welab.wefe.board.service.database.entity.base.AbstractBaseMySqlModel', 'com.welab.wefe.common.wefe.enums.AuditStatus', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'javax.persistence.Entity', 'javax.persistence.EnumType', 'javax.persistence.Enumerated'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| ProjectMemberMySqlModel | class |  |



## 类 ProjectMemberMySqlModel

|      |      |
|------|------|
| 访问范围 | @Entity(name = "project_member");public |
| 类型 | class |
| 名称 | ProjectMemberMySqlModel |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
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

### 方法列表

| 名称  | 类型  | 说明 |
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




