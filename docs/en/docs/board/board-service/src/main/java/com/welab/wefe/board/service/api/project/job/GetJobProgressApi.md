# Basic Information

|      |      |
|------|------|
| Name | GetJobProgressApi |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/api/project/job/GetJobProgressApi.java |
| Package Name | com.welab.wefe.board.service.api.project.job |
| Dependencies | ['com.welab.wefe.board.service.api.gateway.GetMemberJobProgressApi', 'com.welab.wefe.board.service.dto.entity.job.JobMemberOutputModel', 'com.welab.wefe.board.service.dto.vo.JobProgressOutput', 'com.welab.wefe.board.service.service.CacheObjects', 'com.welab.wefe.board.service.service.FlowJobService', 'com.welab.wefe.board.service.service.GatewayService', 'com.welab.wefe.board.service.service.JobMemberService', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.fieldvalidate.annotation.Check', 'com.welab.wefe.common.web.api.base.AbstractApi', 'com.welab.wefe.common.web.api.base.Api', 'com.welab.wefe.common.web.dto.AbstractApiInput', 'com.welab.wefe.common.web.dto.ApiResult', 'org.springframework.beans.factory.annotation.Autowired', 'java.util.ArrayList', 'java.util.List'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| GetJobProgressApi | class |  |



## Class GetJobProgressApi

|      |      |
|------|------|
| Access Modifier | @Api(path = "flow/job/get_progress", name = "Get job execution progress of all members", allowAccessWithSign = true);public |
| Type | class |
| Name | GetJobProgressApi |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| jobMemberService | JobMemberService |  |
| flowJobService | FlowJobService |  |
| gatewayService | GatewayService |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| handle | ApiResult<List<JobProgressOutput>> |  |




