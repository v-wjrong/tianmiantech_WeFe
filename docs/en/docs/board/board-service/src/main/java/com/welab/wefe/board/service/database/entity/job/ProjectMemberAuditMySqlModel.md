# Basic Information

|      |      |
|------|------|
| Name | ProjectMemberAuditMySqlModel |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/database/entity/job/ProjectMemberAuditMySqlModel.java |
| Package Name | com.welab.wefe.board.service.database.entity.job |
| Dependencies | ['com.welab.wefe.board.service.database.entity.base.AbstractBaseMySqlModel', 'com.welab.wefe.common.wefe.enums.AuditStatus', 'javax.persistence.Entity', 'javax.persistence.EnumType', 'javax.persistence.Enumerated'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| ProjectMemberAuditMySqlModel | class |  |



## Class ProjectMemberAuditMySqlModel

|      |      |
|------|------|
| Access Modifier | @Entity(name = "project_member_audit");public |
| Type | class |
| Name | ProjectMemberAuditMySqlModel |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| memberId | String |  |
| auditComment | String |  |
| projectId | String |  |
| auditResult | AuditStatus |  |
| auditorId | String |  |
| serialVersionUID = 8870060097218263816L | long |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getProjectId | String |  |
| setAuditorId | void |  |
| setProjectId | void |  |
| getMemberId | String |  |
| getAuditResult | AuditStatus |  |
| getAuditorId | String |  |
| setMemberId | void |  |
| setAuditResult | void |  |
| getAuditComment | String |  |
| setAuditComment | void |  |




