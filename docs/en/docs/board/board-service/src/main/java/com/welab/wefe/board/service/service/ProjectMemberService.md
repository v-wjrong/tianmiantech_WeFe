# Basic Information

|      |      |
|------|------|
| Name | ProjectMemberService |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/ProjectMemberService.java |
| Package Name | com.welab.wefe.board.service.service |
| Dependencies | ['com.welab.wefe.board.service.api.project.member.AddApi', 'com.welab.wefe.board.service.api.project.member.ListInProjectApi', 'com.welab.wefe.board.service.database.entity.job', 'com.welab.wefe.board.service.database.repository.ProjectMemberAuditRepository', 'com.welab.wefe.board.service.database.repository.ProjectMemberRepository', 'com.welab.wefe.board.service.dto.entity.ProjectMemberInput', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.data.mysql.Where', 'com.welab.wefe.common.data.mysql.enums.OrderBy', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.web.util.CurrentAccountUtil', 'com.welab.wefe.common.wefe.enums.AuditStatus', 'com.welab.wefe.common.wefe.enums.FederatedLearningType', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'org.apache.commons.collections4.CollectionUtils', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.data.jpa.domain.Specification', 'org.springframework.stereotype.Service', 'org.springframework.transaction.annotation.Transactional', 'java.util.ArrayList', 'java.util.HashSet', 'java.util.List', 'java.util.Set', 'java.util.function.Consumer', 'java.util.function.Function', 'java.util.stream.Collectors'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| ProjectMemberService | class |  |



## Class ProjectMemberService

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | ProjectMemberService |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| jobMemberService | JobMemberService |  |
| projectMemberAuditRepository | ProjectMemberAuditRepository |  |
| jobService | JobService |  |
| messageService | MessageService |  |
| projectDataSetService | ProjectDataSetService |  |
| projectMemberRepo | ProjectMemberRepository |  |
| LOG = LoggerFactory.getLogger(this.getClass()) | Logger |  |
| gatewayService | GatewayService |  |
| projectService | ProjectService |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| update | ProjectMemberMySqlModel |  |
| updateProjectMember | ProjectMemberMySqlModel |  |
| findOneByMemberId | ProjectMemberMySqlModel |  |
| addProviderMember | void |  |
| checkMembers | boolean |  |
| addPromoterMember | void |  |
| addMember | void |  |
| checkExistMember | boolean |  |
| findListByProjectId | List<ProjectMemberMySqlModel> |  |
| listFormalProjectMembers | List<ProjectMemberMySqlModel> |  |
| findListByMemberId | List<ProjectMemberMySqlModel> |  |
| findList | List<ProjectMemberMySqlModel> |  |
| listFormalProjectProviders | List<ProjectMemberMySqlModel> |  |




