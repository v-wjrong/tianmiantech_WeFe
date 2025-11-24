# 基础信息

|      |      |
|------|------|
| 名称 | ProjectMemberOutputModel |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/dto/entity/project/ProjectMemberOutputModel.java |
| 包名 | com.welab.wefe.board.service.dto.entity.project |
| 依赖项 | ['com.welab.wefe.board.service.dto.entity.AbstractOutputModel', 'com.welab.wefe.board.service.service.CacheObjects', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.fieldvalidate.annotation.Check', 'com.welab.wefe.common.wefe.enums.AuditStatus', 'com.welab.wefe.common.wefe.enums.JobMemberRole'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| ProjectMemberOutputModel | class |  |



## 类 ProjectMemberOutputModel

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | ProjectMemberOutputModel |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| exited = false | boolean |  |
| auditStatus | AuditStatus |  |
| projectId | String |  |
| auditStatusFromMyself | AuditStatus |  |
| memberId | String |  |
| auditStatusFromOthers | AuditStatus |  |
| fromCreateProject | boolean |  |
| inviterId | String |  |
| auditComment | String |  |
| memberRole | JobMemberRole |  |
| inviterName | String |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| setInviterId | void |  |
| setAuditStatusFromMyself | void |  |
| isFromCreateProject | boolean |  |
| setMemberId | void |  |
| setAuditStatus | void |  |
| getAuditStatusFromOthers | AuditStatus |  |
| setInviterName | void |  |
| getInviterId | String |  |
| getMemberName | String |  |
| getInviterName | String |  |
| getAuditComment | String |  |
| setFromCreateProject | void |  |
| setAuditComment | void |  |
| getAuditStatusFromMyself | AuditStatus |  |
| setAuditStatusFromOthers | void |  |
| getAuditStatus | AuditStatus |  |
| getProjectId | String |  |
| setProjectId | void |  |
| getMemberId | String |  |
| getMemberRole | JobMemberRole |  |
| setMemberRole | void |  |
| isExited | boolean |  |
| setExited | void |  |




