# Basic Information

|      |      |
|------|------|
| Name | ProjectFlowService |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/ProjectFlowService.java |
| Package Name | com.welab.wefe.board.service.service |
| Dependencies | ['com.alibaba.fastjson.JSON', 'com.alibaba.fastjson.JSONArray', 'com.alibaba.fastjson.JSONObject', 'com.welab.wefe.board.service.api.project.flow', 'com.welab.wefe.board.service.api.project.job.OnJobFinishedApi', 'com.welab.wefe.board.service.api.project.modeling.DetailApi', 'com.welab.wefe.board.service.api.project.modeling.QueryApi', 'com.welab.wefe.board.service.api.project.node.UpdateApi', 'com.welab.wefe.board.service.component.Components', 'com.welab.wefe.board.service.database.entity.flow.FlowTemplateMySqlModel', 'com.welab.wefe.board.service.database.entity.job', 'com.welab.wefe.board.service.database.repository', 'com.welab.wefe.board.service.dto.base.PagingOutput', 'com.welab.wefe.board.service.dto.entity.job.ProjectFlowNodeOutputModel', 'com.welab.wefe.board.service.dto.entity.job.TaskResultOutputModel', 'com.welab.wefe.board.service.dto.entity.modeling_config.ModelingInfoOutputModel', 'com.welab.wefe.board.service.dto.entity.project.ProjectFlowListOutputModel', 'com.welab.wefe.board.service.dto.entity.project.ProjectFlowProgressOutputModel', 'com.welab.wefe.board.service.dto.kernel.machine_learning.TaskConfig', 'com.welab.wefe.board.service.onlinedemo.OnlineDemoBranchStrategy', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.data.mysql.Where', 'com.welab.wefe.common.data.mysql.enums.OrderBy', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.DateUtil', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.web.util.CurrentAccountUtil', 'com.welab.wefe.common.web.util.ModelMapper', 'com.welab.wefe.common.wefe.enums', 'org.apache.commons.collections4.CollectionUtils', 'org.apache.commons.lang3.StringUtils', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.beans.BeanUtils', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.data.jpa.domain.Specification', 'org.springframework.stereotype.Service', 'org.springframework.transaction.annotation.Transactional', 'java.util', 'java.util.stream.Collectors'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| ProjectFlowService | class |  |



## Class ProjectFlowService

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | ProjectFlowService |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| taskRepository | TaskRepository |  |
| jobRepository | JobRepository |  |
| LOG = LoggerFactory.getLogger(this.getClass()) | Logger |  |
| taskResultService | TaskResultService |  |
| jobService | JobService |  |
| projectService | ProjectService |  |
| modelOotRecordService | ModelOotRecordService |  |
| projectFlowRepo | ProjectFlowRepository |  |
| projectFlowNodeRepository | ProjectFlowNodeRepository |  |
| projectMemberService | ProjectMemberService |  |
| taskService | TaskService |  |
| flowTemplateService | FlowTemplateService |  |
| taskResultRepository | TaskResultRepository |  |
| projectFlowNodeService | ProjectFlowNodeService |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| findFlowsByProjectId | List<ProjectFlowMySqlModel> |  |
| updateFlowStatus | void |  |
| addOotFlow | AddOotFlowApi.Output |  |
| isCalculateScoreDistribution | boolean |  |
| getParamsIsNullFlowNodes | List<ProjectFlowNodeOutputModel> |  |
| handleJobWithGridSearch | void |  |
| updateFlowGraph | void |  |
| top | void |  |
| delete | void |  |
| updateOldParams | void |  |
| queryModelingInfo | PagingOutput<ModelingInfoOutputModel> |  |
| query | PagingOutput<ProjectFlowListOutputModel> |  |
| findModelingResult | TaskResultOutputModel |  |
| flowFinished | void |  |
| updateFlowBaseInfo | void |  |
| getFlowNodes | List<ProjectFlowNodeOutputModel> |  |
| copy | void |  |
| findOne | ProjectFlowMySqlModel |  |
| addFlow | String |  |
| getProgress | List<ProjectFlowProgressOutputModel> |  |
| graphNodeToFlowNode | ProjectFlowNodeMySqlModel |  |




