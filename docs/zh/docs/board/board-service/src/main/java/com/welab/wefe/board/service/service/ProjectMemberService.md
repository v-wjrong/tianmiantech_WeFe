# 基础信息

|      |      |
|------|------|
| 名称 | ProjectMemberService |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/ProjectMemberService.java |
| 包名 | com.welab.wefe.board.service.service |
| 依赖项 | ['com.welab.wefe.board.service.api.project.member.AddApi', 'com.welab.wefe.board.service.api.project.member.ListInProjectApi', 'com.welab.wefe.board.service.database.entity.job', 'com.welab.wefe.board.service.database.repository.ProjectMemberAuditRepository', 'com.welab.wefe.board.service.database.repository.ProjectMemberRepository', 'com.welab.wefe.board.service.dto.entity.ProjectMemberInput', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.data.mysql.Where', 'com.welab.wefe.common.data.mysql.enums.OrderBy', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.web.util.CurrentAccountUtil', 'com.welab.wefe.common.wefe.enums.AuditStatus', 'com.welab.wefe.common.wefe.enums.FederatedLearningType', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'org.apache.commons.collections4.CollectionUtils', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.data.jpa.domain.Specification', 'org.springframework.stereotype.Service', 'org.springframework.transaction.annotation.Transactional', 'java.util.ArrayList', 'java.util.HashSet', 'java.util.List', 'java.util.Set', 'java.util.function.Consumer', 'java.util.function.Function', 'java.util.stream.Collectors'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| ProjectMemberService | class |  |



## 类 ProjectMemberService

|      |      |
|------|------|
| 访问范围 | @Service;public |
| 类型 | class |
| 名称 | ProjectMemberService |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
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

### 方法列表

| 名称  | 类型  | 说明 |
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




