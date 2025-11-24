# Basic Information

|      |      |
|------|------|
| Name | TaskProgressDetailApi |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/api/project/job/task/TaskProgressDetailApi.java |
| Package Name | com.welab.wefe.board.service.api.project.job.task |
| Dependencies | ['com.welab.wefe.board.service.database.entity.job.TaskProgressMysqlModel', 'com.welab.wefe.board.service.dto.entity.job.TaskProgressOuputModel', 'com.welab.wefe.board.service.service.TaskProgressService', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.fieldvalidate.annotation.Check', 'com.welab.wefe.common.web.api.base.AbstractApi', 'com.welab.wefe.common.web.api.base.Api', 'com.welab.wefe.common.web.dto.AbstractApiInput', 'com.welab.wefe.common.web.dto.ApiResult', 'com.welab.wefe.common.web.util.ModelMapper', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'org.springframework.beans.factory.annotation.Autowired'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| TaskProgressDetailApi | class |  |



## Class TaskProgressDetailApi

|      |      |
|------|------|
| Access Modifier | @Api(path = "task/progress/detail", name = "task progress details");public |
| Type | class |
| Name | TaskProgressDetailApi |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| taskProgressService | TaskProgressService |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| handle | ApiResult<TaskProgressOuputModel> |  |




