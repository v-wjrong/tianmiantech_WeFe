# 基础信息

|      |      |
|------|------|
| 名称 | GatewayService |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/GatewayService.java |
| 包名 | com.welab.wefe.board.service.service |
| 依赖项 | ['com.alibaba.fastjson.JSONObject', 'com.welab.wefe.board.service.api.project.flow', 'com.welab.wefe.board.service.api.project.node.UpdateApi', 'com.welab.wefe.board.service.api.project.project.AddApi', 'com.welab.wefe.board.service.api.service.AliveApi', 'com.welab.wefe.board.service.database.entity.job.JobMemberMySqlModel', 'com.welab.wefe.board.service.database.entity.job.ProjectFlowMySqlModel', 'com.welab.wefe.board.service.database.entity.job.ProjectMemberMySqlModel', 'com.welab.wefe.board.service.database.repository.JobMemberRepository', 'com.welab.wefe.board.service.exception.MemberGatewayException', 'com.welab.wefe.board.service.service.globalconfig.GlobalConfigService', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.web.api.base.Api', 'com.welab.wefe.common.web.dto.AbstractApiInput', 'com.welab.wefe.common.web.dto.ApiResult', 'com.welab.wefe.common.wefe.checkpoint.dto.ServiceAvailableCheckOutput', 'com.welab.wefe.common.wefe.dto.global_config.GatewayConfigModel', 'com.welab.wefe.common.wefe.enums.AuditStatus', 'com.welab.wefe.common.wefe.enums.FederatedLearningType', 'com.welab.wefe.common.wefe.enums.GatewayProcessorType', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'net.jodah.expiringmap.ExpiringMap', 'org.apache.commons.lang.StringUtils', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.stereotype.Service', 'java.util.List', 'java.util.concurrent.TimeUnit', 'java.util.stream.Collectors'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| GatewayService | class |  |



## 类 GatewayService

|      |      |
|------|------|
| 访问范围 | @Service;public |
| 类型 | class |
| 名称 | GatewayService |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| jobMemberService | JobMemberService |  |
| jobMemberRepo | JobMemberRepository |  |
| projectFlowService | ProjectFlowService |  |
| projectMemberService | ProjectMemberService |  |
| messageService | MessageService |  |
| globalConfigService | GlobalConfigService |  |
| CACHE_MAP = ExpiringMap.builder().expiration(60, TimeUnit.SECONDS).maxSize(500).build() | ExpiringMap<String, Object> |  |

### 方法列表

| 名称  | 类型  | 说明 |
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




