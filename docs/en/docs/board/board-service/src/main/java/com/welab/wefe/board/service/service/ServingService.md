# Basic Information

|      |      |
|------|------|
| Name | ServingService |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/ServingService.java |
| Package Name | com.welab.wefe.board.service.service |
| Dependencies | ['com.alibaba.fastjson.JSON', 'com.alibaba.fastjson.JSONObject', 'com.welab.wefe.board.service.api.data_output_info.PushModelToServingByProviderApi', 'com.welab.wefe.board.service.component.EvaluationComponent', 'com.welab.wefe.board.service.component.modeling.ScoreCardComponent', 'com.welab.wefe.board.service.database.entity.job.JobMySqlModel', 'com.welab.wefe.board.service.database.entity.job.TaskMySqlModel', 'com.welab.wefe.board.service.database.entity.job.TaskResultMySqlModel', 'com.welab.wefe.board.service.database.repository.JobRepository', 'com.welab.wefe.board.service.dto.entity.job.JobMemberOutputModel', 'com.welab.wefe.board.service.dto.serving.ProviderModelPushResult', 'com.welab.wefe.board.service.service.globalconfig.GlobalConfigService', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.constant.SecretKeyType', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.http.HttpRequest', 'com.welab.wefe.common.http.HttpResponse', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.util.RSAUtil', 'com.welab.wefe.common.util.SignUtil', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.wefe.dto.global_config.MemberInfoModel', 'com.welab.wefe.common.wefe.dto.global_config.ServingConfigModel', 'com.welab.wefe.common.wefe.enums.Algorithm', 'com.welab.wefe.common.wefe.enums.ComponentType', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'com.welab.wefe.common.wefe.enums.TaskResultType', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.stereotype.Service', 'java.util.List', 'java.util.Map', 'java.util.TreeMap', 'java.util.stream.Collectors'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| ServingService | class |  |



## Class ServingService

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | ServingService |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| gatewayService | GatewayService |  |
| jobMemberService | JobMemberService |  |
| globalConfigService | GlobalConfigService |  |
| jobRepository | JobRepository |  |
| taskResultService | TaskResultService |  |
| taskService | TaskService |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getScoresDistribution | Object |  |
| callOtherMemberPushServing | void |  |
| syncModelToServing | Object |  |
| buildModelParams | TreeMap<String, Object> |  |
| getMembersByJobId | List<JSONObject> |  |
| getFeatureEngineerMap | Map<Integer, Object> |  |
| refreshMemberInfo | void |  |
| main | void |  |
| request | JSONObject |  |
| getScoreCardInfo | Object |  |
| getMemberListByTaskIdAndRole | List<JobMemberOutputModel> |  |
| getModelParam | JObject |  |
| callMembersPushToServing | List<ProviderModelPushResult> |  |
| getMemberListByJobId | List<JobMemberOutputModel> |  |
| pushRsaKeyToServing | void |  |
| request | JSONObject |  |
| callSingleMemberPushToServing | ProviderModelPushResult |  |
| check | void |  |
| extractProviderTaskId | String |  |
| pushToServing | void |  |
| extractName | String |  |
| getByJobId | JobMySqlModel |  |
| fillPublicKey | List<JSONObject> |  |
| getModelIdByTaskIdAndRole | String |  |
| getTaskResult | TaskResultMySqlModel |  |
| getAlgorithm | Algorithm |  |
| getModelParam | String |  |




