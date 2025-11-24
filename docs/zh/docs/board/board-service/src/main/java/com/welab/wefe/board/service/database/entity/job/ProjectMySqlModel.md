# 基础信息

|      |      |
|------|------|
| 名称 | ProjectMySqlModel |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/database/entity/job/ProjectMySqlModel.java |
| 包名 | com.welab.wefe.board.service.database.entity.job |
| 依赖项 | ['com.welab.wefe.board.service.database.entity.base.AbstractBaseMySqlModel', 'com.welab.wefe.common.wefe.enums.AuditStatus', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'com.welab.wefe.common.wefe.enums.ProjectType', 'javax.persistence.Entity', 'javax.persistence.EnumType', 'javax.persistence.Enumerated', 'java.util.Date'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| ProjectMySqlModel | class |  |



## 类 ProjectMySqlModel

|      |      |
|------|------|
| 访问范围 | @Entity(name = "project");public |
| 类型 | class |
| 名称 | ProjectMySqlModel |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
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

### 方法列表

| 名称  | 类型  | 说明 |
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




