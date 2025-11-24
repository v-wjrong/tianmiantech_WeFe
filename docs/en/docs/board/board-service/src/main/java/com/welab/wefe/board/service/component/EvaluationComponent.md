# Basic Information

|      |      |
|------|------|
| Name | EvaluationComponent |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/component/EvaluationComponent.java |
| Package Name | com.welab.wefe.board.service.component |
| Dependencies | ['com.alibaba.fastjson.JSONObject', 'com.welab.wefe.board.service.api.project.node.UpdateApi', 'com.welab.wefe.board.service.component.base.AbstractComponent', 'com.welab.wefe.board.service.component.base.io', 'com.welab.wefe.board.service.component.enums.EvaluationType', 'com.welab.wefe.board.service.database.entity.job.TaskMySqlModel', 'com.welab.wefe.board.service.database.entity.job.TaskResultMySqlModel', 'com.welab.wefe.board.service.exception.FlowNodeException', 'com.welab.wefe.board.service.model.FlowGraph', 'com.welab.wefe.board.service.model.FlowGraphNode', 'com.welab.wefe.board.service.model.JobBuilder', 'com.welab.wefe.board.service.service.TaskService', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.fieldvalidate.AbstractCheckModel', 'com.welab.wefe.common.fieldvalidate.annotation.Check', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.web.util.ModelMapper', 'com.welab.wefe.common.wefe.enums.ComponentType', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'com.welab.wefe.common.wefe.enums.TaskResultType', 'org.apache.commons.collections4.CollectionUtils', 'org.apache.commons.compress.utils.Lists', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.stereotype.Service', 'java.math.BigDecimal', 'java.util.ArrayList', 'java.util.Arrays', 'java.util.List', 'java.util.stream.Collectors'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| EvaluationComponent | class |  |



## Class EvaluationComponent

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | EvaluationComponent |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| taskService | TaskService |  |
| updateApi | UpdateApi |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| taskType | ComponentType |  |
| extractYAxis | int |  |
| parserScoresDistributionCurveData | JObject |  |
| extractFlowNodeId | String |  |
| extractNormalName | String |  |
| extractYAxis2 | double |  |
| precisionProcessByDouble | double |  |
| extractSuffix | String |  |
| findEvaluationTrainTaskResultByTaskId | TaskResultMySqlModel |  |
| getAllResult | List<TaskResultMySqlModel> |  |
| getValidateObjByTaskId | JObject |  |
| extractPreTrainName | String |  |
| extractXAxis | String |  |
| getPsiObjByTaskId | JObject |  |
| getTrainJObject | JObject |  |
| findEvaluationValidateTaskResultByTaskId | TaskResultMySqlModel |  |
| checkBeforeBuildTask | void |  |
| getValidateJObject | JObject |  |
| findEvaluationTaskByTaskResult | TaskMySqlModel |  |
| getResult | TaskResultMySqlModel |  |
| findPsiTaskResultByTaskId | TaskResultMySqlModel |  |
| findEvaluationDistributionTaskResultByTaskId | TaskResultMySqlModel |  |
| extractPreValidateName | String |  |
| precisionProcessByString | double |  |
| getResultByType | JObject |  |
| extractModelComponentType | String |  |
| findEvaluationTaskResultByTaskId | TaskResultMySqlModel |  |
| parserTopN | JObject |  |
| getDistributionObjByTaskId | JObject |  |
| getTrainObjByTaskId | JObject |  |
| parserTrainCurveData | JObject |  |
| parserValidateCurveData | JObject |  |
| createTaskParams | JSONObject |  |
| extractScoreDistributionData | JObject |  |
| scoreDistributionKey | String |  |
| parserCurveData | JObject |  |
| normalizerData | JObject |  |
| inputs | List<InputMatcher> |  |
| outputs | List<OutputItem> |  |




