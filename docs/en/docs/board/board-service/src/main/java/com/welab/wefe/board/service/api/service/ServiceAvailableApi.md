# Basic Information

|      |      |
|------|------|
| Name | ServiceAvailableApi |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/api/service/ServiceAvailableApi.java |
| Package Name | com.welab.wefe.board.service.api.service |
| Dependencies | ['com.welab.wefe.board.service.service.ServiceCheckService', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.fieldvalidate.annotation.Check', 'com.welab.wefe.common.web.api.base.AbstractApi', 'com.welab.wefe.common.web.api.base.Api', 'com.welab.wefe.common.web.dto.AbstractApiInput', 'com.welab.wefe.common.web.dto.ApiResult', 'com.welab.wefe.common.wefe.checkpoint.dto.ServiceAvailableCheckOutput', 'com.welab.wefe.common.wefe.enums.ServiceType', 'org.springframework.beans.factory.annotation.Autowired', 'java.io.IOException'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| ServiceAvailableApi | class |  |



## Class ServiceAvailableApi

|      |      |
|------|------|
| Access Modifier | @Api(path = "service/available", name = "list all checkpoint in board service to show its availability.");public |
| Type | class |
| Name | ServiceAvailableApi |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| serviceCheckService | ServiceCheckService |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| handle | ApiResult<ServiceAvailableCheckOutput> |  |




