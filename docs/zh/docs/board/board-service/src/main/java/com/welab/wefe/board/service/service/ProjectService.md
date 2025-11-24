# 基础信息

|      |      |
|------|------|
| 名称 | ProjectService |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/ProjectService.java |
| 包名 | com.welab.wefe.board.service.service |
| 依赖项 | ['com.welab.wefe.board.service.api.project.dataset.AddDataSetApi', 'com.welab.wefe.board.service.api.project.dataset.RemoveDataSetApi', 'com.welab.wefe.board.service.api.project.member.ExitProjectApi', 'com.welab.wefe.board.service.api.project.member.ListInProjectApi', 'com.welab.wefe.board.service.api.project.member.RemoveApi', 'com.welab.wefe.board.service.api.project.project', 'com.welab.wefe.board.service.database.entity.job', 'com.welab.wefe.board.service.database.repository', 'com.welab.wefe.board.service.dto.base.PagingOutput', 'com.welab.wefe.board.service.dto.entity.ProjectDataSetInput', 'com.welab.wefe.board.service.dto.entity.ProjectMemberInput', 'com.welab.wefe.board.service.dto.entity.project.ProjectDetailMemberOutputModel', 'com.welab.wefe.board.service.dto.entity.project.ProjectMemberOutputModel', 'com.welab.wefe.board.service.dto.entity.project.ProjectOutputModel', 'com.welab.wefe.board.service.dto.entity.project.ProjectQueryOutputModel', 'com.welab.wefe.board.service.dto.entity.project.data_set.ProjectDataResourceOutputModel', 'com.welab.wefe.board.service.dto.vo.AuditStatusCounts', 'com.welab.wefe.board.service.dto.vo.ProjectFlowStatisticsResult', 'com.welab.wefe.board.service.dto.vo.RoleCounts', 'com.welab.wefe.board.service.onlinedemo.OnlineDemoBranchStrategy', 'com.welab.wefe.board.service.service.account.AccountService', 'com.welab.wefe.board.service.service.data_resource.DataResourceService', 'com.welab.wefe.common.Convert', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.data.mysql.Where', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.util.ThreadUtil', 'com.welab.wefe.common.web.dto.AbstractApiInput', 'com.welab.wefe.common.web.util.CurrentAccountUtil', 'com.welab.wefe.common.web.util.ModelMapper', 'com.welab.wefe.common.wefe.enums.AuditStatus', 'com.welab.wefe.common.wefe.enums.FederatedLearningType', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'com.welab.wefe.common.wefe.enums.ProjectFlowStatus', 'org.apache.commons.collections4.CollectionUtils', 'org.apache.commons.lang3.StringUtils', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.data.jpa.domain.Specification', 'org.springframework.stereotype.Service', 'org.springframework.transaction.annotation.Transactional', 'java.util', 'java.util.stream.Collectors'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| ProjectService | class |  |



## 类 ProjectService

|      |      |
|------|------|
| 访问范围 | @Service;public |
| 类型 | class |
| 名称 | ProjectService |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| projectFlowRepository | ProjectFlowRepository |  |
| projectFlowService | ProjectFlowService |  |
| projectMemberAuditService | ProjectMemberAuditService |  |
| projectFlowNodeService | ProjectFlowNodeService |  |
| projectDataSetRepo | ProjectDataSetRepository |  |
| jobService | JobService |  |
| projectMemberRepo | ProjectMemberRepository |  |
| projectRepo | ProjectRepository |  |
| projectDataSetService | ProjectDataSetService |  |
| projectMemberAuditRepository | ProjectMemberAuditRepository |  |
| messageService | MessageService |  |
| projectMemberService | ProjectMemberService |  |
| accountService | AccountService |  |
| projectFlowNodeRepository | ProjectFlowNodeRepository |  |
| dataResourceService | DataResourceService |  |
| projectService | ProjectService |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| top | void |  |
| buildQueryWhere | String |  |
| findByProjectId | ProjectMySqlModel |  |
| removeMember | void |  |
| getPromoterDataInfo | DataInfoApi.Output |  |
| statistics | CountStatisticsApi.Output |  |
| syncAuditProjectInfo | void |  |
| buildJobOutputModel | ProjectQueryOutputModel |  |
| checkAuditingRecord | void |  |
| getDataInfo | DataInfoApi.Output |  |
| updateProject | void |  |
| query | PagingOutput<ProjectQueryOutputModel> |  |
| pullNewestProjectInfo | void |  |
| removeDataSet | void |  |
| addProjectDataSet | ProjectMySqlModel |  |
| detail | ProjectOutputModel |  |
| auditProject | void |  |
| closeProject | void |  |
| addProject | String |  |
| exitProject | void |  |
| updateFlowStatusStatistics | void |  |
| findProjectByJobId | ProjectMySqlModel |  |




