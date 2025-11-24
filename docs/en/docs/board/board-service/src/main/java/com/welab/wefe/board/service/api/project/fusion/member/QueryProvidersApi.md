# Basic Information

|      |      |
|------|------|
| Name | QueryProvidersApi |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/api/project/fusion/member/QueryProvidersApi.java |
| Package Name | com.welab.wefe.board.service.api.project.fusion.member |
| Dependencies | ['com.welab.wefe.board.service.database.entity.job.ProjectMemberMySqlModel', 'com.welab.wefe.board.service.dto.entity.project.ProjectMemberOutputModel', 'com.welab.wefe.board.service.service.ProjectMemberService', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.fieldvalidate.annotation.Check', 'com.welab.wefe.common.web.api.base.AbstractApi', 'com.welab.wefe.common.web.api.base.Api', 'com.welab.wefe.common.web.dto.AbstractApiInput', 'com.welab.wefe.common.web.dto.ApiResult', 'com.welab.wefe.common.web.util.ModelMapper', 'org.springframework.beans.factory.annotation.Autowired', 'java.io.IOException', 'java.util.List'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| QueryProvidersApi | class |  |



## Class QueryProvidersApi

|      |      |
|------|------|
| Access Modifier | @Api(path = "fusion/query/providers",;        name = "query provider list",;        desc = "query provider list";);public |
| Type | class |
| Name | QueryProvidersApi |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| projectMemberService | ProjectMemberService |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| handle | ApiResult<List<ProjectMemberOutputModel>> |  |




