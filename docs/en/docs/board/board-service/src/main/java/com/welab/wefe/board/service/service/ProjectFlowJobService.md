# Basic Information

|      |      |
|------|------|
| Name | ProjectFlowJobService |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/ProjectFlowJobService.java |
| Package Name | com.welab.wefe.board.service.service |
| Dependencies | ['com.alibaba.fastjson.JSONObject', 'com.welab.wefe.board.service.api.project.flow.StartFlowApi', 'com.welab.wefe.board.service.api.project.job.ResumeJobApi', 'com.welab.wefe.board.service.api.project.job.StopJobApi', 'com.welab.wefe.board.service.component.Components', 'com.welab.wefe.board.service.component.DataIOComponent', 'com.welab.wefe.board.service.component.OotComponent', 'com.welab.wefe.board.service.component.base.AbstractComponent', 'com.welab.wefe.board.service.component.base.dto.AbstractDataIOParam', 'com.welab.wefe.board.service.component.base.dto.AbstractDataSetItem', 'com.welab.wefe.board.service.database.entity.data_resource.TableDataSetMysqlModel', 'com.welab.wefe.board.service.database.entity.job', 'com.welab.wefe.board.service.database.repository', 'com.welab.wefe.board.service.dto.entity.data_resource.output.DataResourceOutputModel', 'com.welab.wefe.board.service.dto.entity.data_resource.output.TableDataSetOutputModel', 'com.welab.wefe.board.service.dto.kernel.Member', 'com.welab.wefe.board.service.dto.kernel.machine_learning.Env', 'com.welab.wefe.board.service.dto.kernel.machine_learning.JobDataSet', 'com.welab.wefe.board.service.dto.kernel.machine_learning.KernelJob', 'com.welab.wefe.board.service.dto.kernel.machine_learning.Project', 'com.welab.wefe.board.service.dto.vo.JobArbiterInfo', 'com.welab.wefe.board.service.exception.FlowNodeException', 'com.welab.wefe.board.service.model.FlowGraph', 'com.welab.wefe.board.service.model.FlowGraphNode', 'com.welab.wefe.board.service.model.JobBuilder', 'com.welab.wefe.board.service.service.data_resource.DataResourceService', 'com.welab.wefe.board.service.service.data_resource.table_data_set.TableDataSetService', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.DateUtil', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.web.util.CurrentAccountUtil', 'com.welab.wefe.common.wefe.checkpoint.dto.MemberAvailableCheckOutput', 'com.welab.wefe.common.wefe.enums', 'org.apache.commons.collections4.CollectionUtils', 'org.apache.commons.lang3.StringUtils', 'org.springframework.beans.BeanUtils', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.stereotype.Service', 'org.springframework.transaction.annotation.Transactional', 'java.util', 'java.util.stream.Collectors'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| ProjectFlowJobService | class |  |



## Class ProjectFlowJobService

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | ProjectFlowJobService |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| serviceCheckService | ServiceCheckService |  |
| projectFlowRepo | ProjectFlowRepository |  |
| projectFlowNodeService | ProjectFlowNodeService |  |
| taskService | TaskService |  |
| taskResultService | TaskResultService |  |
| flowActionQueueService | FlowActionQueueService |  |
| jobMemberRepo | JobMemberRepository |  |
| jobRepo | JobRepository |  |
| tableDataSetService | TableDataSetService |  |
| projectDataSetService | ProjectDataSetService |  |
| jobService | JobService |  |
| taskResultRepository | TaskResultRepository |  |
| gatewayService | GatewayService |  |
| taskRepository | TaskRepository |  |
| projectService | ProjectService |  |
| projectFlowService | ProjectFlowService |  |
| MIX_FLOW_PROMOTER_NUM = 2 | int |  |
| dataResourceService | DataResourceService |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| copyNodeInfoFromLastJob | TaskMySqlModel |  |
| calcArbiterInfo | JobArbiterInfo |  |
| updateDataSetUsageCountInJob | void |  |
| isCreator | boolean |  |
| resumeJob | void |  |
| copyIterationResult | void |  |
| listJobMembers | List<JobMemberMySqlModel> |  |
| startFlow | String |  |
| stopFlowJob | void |  |
| createJob | JobMySqlModel |  |
| createJobTasks | List<TaskMySqlModel> |  |
| copyMixTaskInfoFromLastJob | List<TaskMySqlModel> |  |
| setJobConfig | void |  |
| listJobDataSets | List<JobDataSet> |  |
| listNodeDataSetItems | List<? extends AbstractDataSetItem> |  |
| checkBeforeStartFlow | void |  |
| addPreTasks | void |  |




