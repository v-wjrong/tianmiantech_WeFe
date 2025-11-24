# 基础信息

|      |      |
|------|------|
| 名称 | Member |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/dto/kernel/Member.java |
| 包名 | com.welab.wefe.board.service.dto.kernel |
| 依赖项 | ['com.welab.wefe.board.service.api.member.GetMemberMachineLearningEnvApi', 'com.welab.wefe.board.service.component.DataIOComponent', 'com.welab.wefe.board.service.database.entity.job.JobMemberMySqlModel', 'com.welab.wefe.board.service.dto.kernel.machine_learning.Env', 'com.welab.wefe.board.service.service.CacheObjects', 'com.welab.wefe.board.service.service.GatewayService', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.web.Launcher', 'com.welab.wefe.common.wefe.enums.FcCloudProvider', 'com.welab.wefe.common.wefe.enums.JobBackendType', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'java.util.ArrayList', 'java.util.List'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| Member | class |  |



## 类 Member

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | Member |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| memberId | String |  |
| memberName | String |  |
| memberRole | JobMemberRole |  |
| backend | JobBackendType |  |
| fcProvider | FcCloudProvider |  |

### 方法列表

| 名称  | 类型  | 说明 |
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




