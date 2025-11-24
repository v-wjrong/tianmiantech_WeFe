# Basic Information

|      |      |
|------|------|
| Name | GetMemberJobProgressApi |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/api/gateway/GetMemberJobProgressApi.java |
| Package Name | com.welab.wefe.board.service.api.gateway |
| Dependencies | ['com.welab.wefe.board.service.dto.vo.JobProgressOutput', 'com.welab.wefe.board.service.service.FlowJobService', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.fieldvalidate.annotation.Check', 'com.welab.wefe.common.web.api.base.AbstractApi', 'com.welab.wefe.common.web.api.base.Api', 'com.welab.wefe.common.web.dto.AbstractApiInput', 'com.welab.wefe.common.web.dto.ApiResult', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'org.springframework.beans.factory.annotation.Autowired'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| GetMemberJobProgressApi | class |  |



## Class GetMemberJobProgressApi

|      |      |
|------|------|
| Access Modifier | @Api(path = "gateway/get_job_progress", name = "get job progress", allowAccessWithSign = true);public |
| Type | class |
| Name | GetMemberJobProgressApi |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| flowJobService | FlowJobService |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| handle | ApiResult<JobProgressOutput> |  |




