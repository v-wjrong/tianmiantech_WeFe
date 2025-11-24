# Basic Information

|      |      |
|------|------|
| Name | DetailFlowApi |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/api/project/flow/DetailFlowApi.java |
| Package Name | com.welab.wefe.board.service.api.project.flow |
| Dependencies | ['com.welab.wefe.board.service.database.entity.job.ModelOotRecordMysqlModel', 'com.welab.wefe.board.service.database.entity.job.ProjectFlowMySqlModel', 'com.welab.wefe.board.service.dto.entity.project.ProjectFlowDetailOutputModel', 'com.welab.wefe.board.service.service.CacheObjects', 'com.welab.wefe.board.service.service.ModelOotRecordService', 'com.welab.wefe.board.service.service.ProjectFlowService', 'com.welab.wefe.board.service.service.ProjectService', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.fieldvalidate.annotation.Check', 'com.welab.wefe.common.web.api.base.AbstractApi', 'com.welab.wefe.common.web.api.base.Api', 'com.welab.wefe.common.web.dto.AbstractApiInput', 'com.welab.wefe.common.web.dto.ApiResult', 'com.welab.wefe.common.web.util.ModelMapper', 'org.springframework.beans.factory.annotation.Autowired'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| DetailFlowApi | class |  |



## Class DetailFlowApi

|      |      |
|------|------|
| Access Modifier | @Api(path = "project/flow/detail", name = "get flow detail");public |
| Type | class |
| Name | DetailFlowApi |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| projectFlowService | ProjectFlowService |  |
| projectService | ProjectService |  |
| modelOotRecordService | ModelOotRecordService |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| handle | ApiResult<ProjectFlowDetailOutputModel> |  |




