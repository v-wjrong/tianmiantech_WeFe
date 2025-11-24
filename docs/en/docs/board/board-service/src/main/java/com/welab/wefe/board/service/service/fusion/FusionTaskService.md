# Basic Information

|      |      |
|------|------|
| Name | FusionTaskService |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/fusion/FusionTaskService.java |
| Package Name | com.welab.wefe.board.service.service.fusion |
| Dependencies | ['com.alibaba.fastjson.JSONObject', 'com.welab.wefe.board.service.api.project.fusion.task', 'com.welab.wefe.board.service.database.entity.data_resource.BloomFilterMysqlModel', 'com.welab.wefe.board.service.database.entity.data_resource.TableDataSetMysqlModel', 'com.welab.wefe.board.service.database.entity.fusion.FusionTaskMySqlModel', 'com.welab.wefe.board.service.database.entity.job.ProjectMySqlModel', 'com.welab.wefe.board.service.database.repository.fusion.FusionTaskRepository', 'com.welab.wefe.board.service.dto.base.PagingOutput', 'com.welab.wefe.board.service.dto.fusion.FusionMemberInfo', 'com.welab.wefe.board.service.dto.fusion.FusionResultExportProgress', 'com.welab.wefe.board.service.dto.fusion.FusionTaskOutput', 'com.welab.wefe.board.service.fusion.actuator.ClientActuator', 'com.welab.wefe.board.service.fusion.actuator.psi.ServerActuator', 'com.welab.wefe.board.service.fusion.manager.ActuatorManager', 'com.welab.wefe.board.service.fusion.manager.ExportManager', 'com.welab.wefe.board.service.onlinedemo.OnlineDemoBranchStrategy', 'com.welab.wefe.board.service.service.AbstractService', 'com.welab.wefe.board.service.service.CacheObjects', 'com.welab.wefe.board.service.service.ProjectService', 'com.welab.wefe.board.service.service.TaskResultService', 'com.welab.wefe.board.service.service.data_resource.DataResourceService', 'com.welab.wefe.board.service.service.data_resource.bloom_filter.BloomFilterService', 'com.welab.wefe.board.service.service.data_resource.table_data_set.TableDataSetService', 'com.welab.wefe.board.service.util.primarykey.PrimaryKeyUtils', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.data.mysql.Where', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.web.util.CurrentAccountUtil', 'com.welab.wefe.common.web.util.ModelMapper', 'com.welab.wefe.common.wefe.enums.AuditStatus', 'com.welab.wefe.common.wefe.enums.DataResourceType', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'com.welab.wefe.fusion.core.enums.AlgorithmType', 'com.welab.wefe.fusion.core.enums.FusionTaskStatus', 'com.welab.wefe.fusion.core.enums.PSIActuatorRole', 'com.welab.wefe.fusion.core.utils.bf.BloomFilterUtils', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.data.jpa.domain.Specification', 'org.springframework.stereotype.Service', 'org.springframework.transaction.annotation.Transactional', 'java.math.BigInteger', 'java.nio.file.Paths', 'java.util.Date', 'java.util.List', 'java.util.UUID', 'java.util.stream.Collectors', 'com.welab.wefe.common.StatusCode.DATA_NOT_FOUND'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| FusionTaskService | class |  |



## Class FusionTaskService

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | FusionTaskService |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| projectService | ProjectService |  |
| tableDataSetService | TableDataSetService |  |
| fieldInfoService | FieldInfoService |  |
| bloomFilterService | BloomFilterService |  |
| thirdPartyService | ThirdPartyService |  |
| fusionTaskRepository | FusionTaskRepository |  |
| dataResourceService | DataResourceService |  |
| taskResultService | TaskResultService |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| update | void |  |
| delete | void |  |
| psiClient | void |  |
| alignByPartner | void |  |
| disAgree | void |  |
| restart | void |  |
| updateByBusinessId | void |  |
| handle | void |  |
| detail | FusionTaskOutput |  |
| psiServer | void |  |
| findByBusinessId | FusionTaskMySqlModel |  |
| updateErrorByBusinessId | void |  |
| AddPsiTask | void |  |
| findByBusinessIdAndStatus | FusionTaskMySqlModel |  |
| paging | PagingOutput<FusionTaskOutput> |  |
| setMemberInfo | void |  |
| add | void |  |
| find | FusionTaskMySqlModel |  |
| psi | void |  |
| deleteCallback | void |  |




