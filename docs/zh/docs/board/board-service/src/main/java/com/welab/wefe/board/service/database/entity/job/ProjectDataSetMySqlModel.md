# 基础信息

|      |      |
|------|------|
| 名称 | ProjectDataSetMySqlModel |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/database/entity/job/ProjectDataSetMySqlModel.java |
| 包名 | com.welab.wefe.board.service.database.entity.job |
| 依赖项 | ['com.welab.wefe.board.service.database.entity.base.AbstractBaseMySqlModel', 'com.welab.wefe.common.wefe.enums.AuditStatus', 'com.welab.wefe.common.wefe.enums.ComponentType', 'com.welab.wefe.common.wefe.enums.DataResourceType', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'javax.persistence.Entity', 'javax.persistence.EnumType', 'javax.persistence.Enumerated', 'java.util.Date'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| ProjectDataSetMySqlModel | class |  |



## 类 ProjectDataSetMySqlModel

|      |      |
|------|------|
| 访问范围 | @Entity(name = "project_data_set");public |
| 类型 | class |
| 名称 | ProjectDataSetMySqlModel |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| serialVersionUID = 7360644396326460699L | long |  |
| dataResourceType | DataResourceType |  |
| projectId | String |  |
| sourceJobId | String |  |
| dataSetId | String |  |
| memberId | String |  |
| sourceType | ComponentType |  |
| auditComment | String |  |
| auditStatus | AuditStatus |  |
| statusUpdatedTime | Date |  |
| sourceTaskId | String |  |
| memberRole | JobMemberRole |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getMemberId | String |  |
| setMemberId | void |  |
| getSourceType | ComponentType |  |
| getStatusUpdatedTime | Date |  |
| setAuditStatus | void |  |
| setMemberRole | void |  |
| getAuditStatus | AuditStatus |  |
| getAuditComment | String |  |
| setStatusUpdatedTime | void |  |
| setAuditComment | void |  |
| getMemberRole | JobMemberRole |  |
| getDataSetId | String |  |
| setDataSetId | void |  |
| getProjectId | String |  |
| setProjectId | void |  |
| setSourceType | void |  |
| getSourceJobId | String |  |
| setSourceJobId | void |  |
| getSourceTaskId | String |  |
| setSourceTaskId | void |  |
| getDataResourceType | DataResourceType |  |
| setDataResourceType | void |  |




