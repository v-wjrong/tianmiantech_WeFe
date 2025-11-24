# 基础信息

|      |      |
|------|------|
| 名称 | ProjectMemberAuditService |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/ProjectMemberAuditService.java |
| 包名 | com.welab.wefe.board.service.service |
| 依赖项 | ['com.welab.wefe.board.service.api.project.member.audit.AuditApi', 'com.welab.wefe.board.service.database.entity.job.ProjectMemberAuditMySqlModel', 'com.welab.wefe.board.service.database.entity.job.ProjectMemberMySqlModel', 'com.welab.wefe.board.service.database.entity.job.ProjectMySqlModel', 'com.welab.wefe.board.service.database.repository.ProjectDataSetRepository', 'com.welab.wefe.board.service.database.repository.ProjectMemberAuditRepository', 'com.welab.wefe.board.service.database.repository.ProjectMemberRepository', 'com.welab.wefe.board.service.database.repository.ProjectRepository', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.data.mysql.Where', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.wefe.enums.AuditStatus', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.data.jpa.domain.Specification', 'org.springframework.stereotype.Service', 'org.springframework.transaction.annotation.Transactional', 'java.util.Date', 'java.util.List'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| ProjectMemberAuditService | class |  |



## 类 ProjectMemberAuditService

|      |      |
|------|------|
| 访问范围 | @Service;public |
| 类型 | class |
| 名称 | ProjectMemberAuditService |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
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

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| allMemberAgreed | boolean |  |
| listAll | List<ProjectMemberAuditMySqlModel> |  |
| findOne | ProjectMemberAuditMySqlModel |  |
| findAllAuditList | List<ProjectMemberAuditMySqlModel> |  |
| auditMember | void |  |




