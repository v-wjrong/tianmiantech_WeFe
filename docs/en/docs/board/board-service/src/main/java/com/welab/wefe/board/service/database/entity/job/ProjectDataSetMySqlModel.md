# Basic Information

|      |      |
|------|------|
| Name | ProjectDataSetMySqlModel |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/database/entity/job/ProjectDataSetMySqlModel.java |
| Package Name | com.welab.wefe.board.service.database.entity.job |
| Dependencies | ['com.welab.wefe.board.service.database.entity.base.AbstractBaseMySqlModel', 'com.welab.wefe.common.wefe.enums.AuditStatus', 'com.welab.wefe.common.wefe.enums.ComponentType', 'com.welab.wefe.common.wefe.enums.DataResourceType', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'javax.persistence.Entity', 'javax.persistence.EnumType', 'javax.persistence.Enumerated', 'java.util.Date'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| ProjectDataSetMySqlModel | class |  |



## Class ProjectDataSetMySqlModel

|      |      |
|------|------|
| Access Modifier | @Entity(name = "project_data_set");public |
| Type | class |
| Name | ProjectDataSetMySqlModel |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
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

### Method List

| Name  | Type  | Description |
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




