# Basic Information

|      |      |
|------|------|
| Name | DataInfoApi |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/api/project/project/DataInfoApi.java |
| Package Name | com.welab.wefe.board.service.api.project.project |
| Dependencies | ['com.welab.wefe.board.service.database.entity.job', 'com.welab.wefe.board.service.service.ProjectService', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.fieldvalidate.annotation.Check', 'com.welab.wefe.common.web.api.base.AbstractApi', 'com.welab.wefe.common.web.api.base.Api', 'com.welab.wefe.common.web.dto.AbstractApiInput', 'com.welab.wefe.common.web.dto.ApiResult', 'org.springframework.beans.factory.annotation.Autowired', 'java.util.List'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| DataInfoApi | class |  |



## Class DataInfoApi

|      |      |
|------|------|
| Access Modifier | @Api(;        path = "project/data/info",;        name = "Get the project and the information in the project",;        desc = "Get the project and the data set, project members, project process, project process node information in the project.";);public |
| Type | class |
| Name | DataInfoApi |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| projectService | ProjectService |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| handle | ApiResult<Output> |  |




