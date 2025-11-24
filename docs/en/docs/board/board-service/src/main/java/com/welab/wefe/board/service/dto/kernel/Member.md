# Basic Information

|      |      |
|------|------|
| Name | Member |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/dto/kernel/Member.java |
| Package Name | com.welab.wefe.board.service.dto.kernel |
| Dependencies | ['com.welab.wefe.board.service.api.member.GetMemberMachineLearningEnvApi', 'com.welab.wefe.board.service.component.DataIOComponent', 'com.welab.wefe.board.service.database.entity.job.JobMemberMySqlModel', 'com.welab.wefe.board.service.dto.kernel.machine_learning.Env', 'com.welab.wefe.board.service.service.CacheObjects', 'com.welab.wefe.board.service.service.GatewayService', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.web.Launcher', 'com.welab.wefe.common.wefe.enums.FcCloudProvider', 'com.welab.wefe.common.wefe.enums.JobBackendType', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'java.util.ArrayList', 'java.util.List'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| Member | class |  |



## Class Member

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | Member |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| memberId | String |  |
| memberName | String |  |
| memberRole | JobMemberRole |  |
| backend | JobBackendType |  |
| fcProvider | FcCloudProvider |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| forMachineLearning | List<Member> |  |
| setMemberId | void |  |
| getMemberRole | JobMemberRole |  |
| forMachineLearning | Member |  |
| getMemberEnv | Env |  |
| getMemberId | String |  |
| buildMachineLearningMember | Member |  |
| getBackend | JobBackendType |  |
| setBackend | void |  |
| forMachineLearning | Member |  |
| setMemberRole | void |  |
| getMemberName | String |  |
| forMachineLearning | Member |  |
| setMemberName | void |  |
| forDeepLearning | List<Member> |  |
| getFcProvider | FcCloudProvider |  |
| setFcProvider | void |  |




