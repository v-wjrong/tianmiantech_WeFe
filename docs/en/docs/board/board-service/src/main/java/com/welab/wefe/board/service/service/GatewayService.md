# Basic Information

|      |      |
|------|------|
| Name | GatewayService |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/GatewayService.java |
| Package Name | com.welab.wefe.board.service.service |
| Dependencies | ['com.alibaba.fastjson.JSONObject', 'com.welab.wefe.board.service.api.project.flow', 'com.welab.wefe.board.service.api.project.node.UpdateApi', 'com.welab.wefe.board.service.api.project.project.AddApi', 'com.welab.wefe.board.service.api.service.AliveApi', 'com.welab.wefe.board.service.database.entity.job.JobMemberMySqlModel', 'com.welab.wefe.board.service.database.entity.job.ProjectFlowMySqlModel', 'com.welab.wefe.board.service.database.entity.job.ProjectMemberMySqlModel', 'com.welab.wefe.board.service.database.repository.JobMemberRepository', 'com.welab.wefe.board.service.exception.MemberGatewayException', 'com.welab.wefe.board.service.service.globalconfig.GlobalConfigService', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.web.api.base.Api', 'com.welab.wefe.common.web.dto.AbstractApiInput', 'com.welab.wefe.common.web.dto.ApiResult', 'com.welab.wefe.common.wefe.checkpoint.dto.ServiceAvailableCheckOutput', 'com.welab.wefe.common.wefe.dto.global_config.GatewayConfigModel', 'com.welab.wefe.common.wefe.enums.AuditStatus', 'com.welab.wefe.common.wefe.enums.FederatedLearningType', 'com.welab.wefe.common.wefe.enums.GatewayProcessorType', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'net.jodah.expiringmap.ExpiringMap', 'org.apache.commons.lang.StringUtils', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.stereotype.Service', 'java.util.List', 'java.util.concurrent.TimeUnit', 'java.util.stream.Collectors'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| GatewayService | class |  |



## Class GatewayService

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | GatewayService |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| jobMemberService | JobMemberService |  |
| jobMemberRepo | JobMemberRepository |  |
| projectFlowService | ProjectFlowService |  |
| projectMemberService | ProjectMemberService |  |
| messageService | MessageService |  |
| globalConfigService | GlobalConfigService |  |
| CACHE_MAP = ExpiringMap.builder().expiration(60, TimeUnit.SECONDS).maxSize(500).build() | ExpiringMap<String, Object> |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| checkBeforeSyncToProjectMembers | void |  |
| syncToOtherJobMembers | void |  |
| checkBeforeSyncToOtherMembers | void |  |
| refreshIpWhiteListCache | void |  |
| refreshPartnerConfigCache | void |  |
| callOtherMemberBoard | void |  |
| checkGatewayAliveProcessor | void |  |
| refreshMemberBlacklistCache | void |  |
| refreshSystemConfigCache | void |  |
| syncToAllMembers | void |  |
| syncToOtherProjectMembers | void |  |
| syncToNotExistedMembers | void |  |
| findMembersByProjectId | List<ProjectMemberMySqlModel> |  |
| callOtherMemberBoard | T |  |
| callOtherMemberBoard | void |  |
| checkBeforeSyncToJobMembers | void |  |
| getLocalGatewayAvailable | ServiceAvailableCheckOutput |  |
| restartExternalGrpcServer | void |  |
| syncToOtherFormalProjectMembers | void |  |
| callOtherMemberBoard | T |  |
| callOtherMemberBoard | T |  |
| callOtherMemberBoard | JSONObject |  |
| checkMemberRouteConnect | void |  |
| pingGatewayAlive | void |  |




