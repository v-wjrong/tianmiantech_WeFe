# Basic Information

|      |      |
|------|------|
| Name | ProjectMemberAuditService |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/ProjectMemberAuditService.java |
| Package Name | com.welab.wefe.board.service.service |
| Dependencies | ['com.welab.wefe.board.service.api.project.member.audit.AuditApi', 'com.welab.wefe.board.service.database.entity.job.ProjectMemberAuditMySqlModel', 'com.welab.wefe.board.service.database.entity.job.ProjectMemberMySqlModel', 'com.welab.wefe.board.service.database.entity.job.ProjectMySqlModel', 'com.welab.wefe.board.service.database.repository.ProjectDataSetRepository', 'com.welab.wefe.board.service.database.repository.ProjectMemberAuditRepository', 'com.welab.wefe.board.service.database.repository.ProjectMemberRepository', 'com.welab.wefe.board.service.database.repository.ProjectRepository', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.data.mysql.Where', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.wefe.enums.AuditStatus', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.data.jpa.domain.Specification', 'org.springframework.stereotype.Service', 'org.springframework.transaction.annotation.Transactional', 'java.util.Date', 'java.util.List'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| ProjectMemberAuditService | class |  |



## Class ProjectMemberAuditService

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | ProjectMemberAuditService |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| projectMemberRepo | ProjectMemberRepository |  |
| projectDataSetService | ProjectDataSetService |  |
| projectService | ProjectService |  |
| projectMemberService | ProjectMemberService |  |
| messageService | MessageService |  |
| gatewayService | GatewayService |  |
| projectDataSetRepo | ProjectDataSetRepository |  |
| projectMemberAuditRepository | ProjectMemberAuditRepository |  |
| projectRepo | ProjectRepository |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| allMemberAgreed | boolean |  |
| listAll | List<ProjectMemberAuditMySqlModel> |  |
| findOne | ProjectMemberAuditMySqlModel |  |
| findAllAuditList | List<ProjectMemberAuditMySqlModel> |  |
| auditMember | void |  |




