# Basic Information

|      |      |
|------|------|
| Name | OotComponent |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/component/OotComponent.java |
| Package Name | com.welab.wefe.board.service.component |
| Dependencies | ['com.alibaba.fastjson.JSON', 'com.alibaba.fastjson.JSONObject', 'com.welab.wefe.board.service.api.project.flow.QueryDataIoTaskConfigApi', 'com.welab.wefe.board.service.api.project.member.ListInProjectApi', 'com.welab.wefe.board.service.component.base.AbstractComponent', 'com.welab.wefe.board.service.component.base.dto.AbstractDataIOParam', 'com.welab.wefe.board.service.component.base.io.IODataType', 'com.welab.wefe.board.service.component.base.io.InputMatcher', 'com.welab.wefe.board.service.component.base.io.Names', 'com.welab.wefe.board.service.component.base.io.OutputItem', 'com.welab.wefe.board.service.constant.Config', 'com.welab.wefe.board.service.database.entity.data_resource.TableDataSetMysqlModel', 'com.welab.wefe.board.service.database.entity.job', 'com.welab.wefe.board.service.dto.kernel.machine_learning.TaskConfig', 'com.welab.wefe.board.service.exception.FlowNodeException', 'com.welab.wefe.board.service.model.FlowGraph', 'com.welab.wefe.board.service.model.FlowGraphNode', 'com.welab.wefe.board.service.model.JobBuilder', 'com.welab.wefe.board.service.service', 'com.welab.wefe.board.service.service.data_resource.table_data_set.TableDataSetService', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.wefe.enums.ComponentType', 'com.welab.wefe.common.wefe.enums.FederatedLearningType', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'com.welab.wefe.common.wefe.enums.TaskResultType', 'org.apache.commons.collections4.CollectionUtils', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.stereotype.Service', 'java.util', 'java.util.stream.Collectors'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| OotComponent | class |  |



## Class OotComponent

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | OotComponent |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| projectFlowNodeService | ProjectFlowNodeService |  |
| config | Config |  |
| gatewayService | GatewayService |  |
| TEMP_UNSUPPORTED_COMPONENT_TYPE_LIST = Arrays.asList(ComponentType.MixLR,            ComponentType.MixSecureBoost, ComponentType.HorzNN, ComponentType.VertNN) | List<ComponentType> |  |
| tableDataSetService | TableDataSetService |  |
| EXCLUDE_COMPONENT_TYPE_LIST = Arrays.asList(ComponentType.FeatureStatistic,            ComponentType.FeatureCalculation, ComponentType.MixStatistic,            ComponentType.Segment, ComponentType.VertPearson, ComponentType.Oot, ComponentType.VertFeaturePSI, ComponentType.VertFilter, ComponentType.ScoreCard) | List<ComponentType> |  |
| projectMemberService | ProjectMemberService |  |
| taskService | TaskService |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getSelectedDataSetItemMap | Map<String, DataIOComponent.DataSetItem> |  |
| checkBeforeBuildTask | void |  |
| createTaskParams | JSONObject |  |
| getEvaluationTaskMySqlModel | TaskMySqlModel |  |
| findDataIoTask | TaskMySqlModel |  |
| checkSelectedMembersValid | void |  |
| checkUnsupportedComponent | void |  |
| getResult | TaskResultMySqlModel |  |
| taskType | ComponentType |  |
| inputs | List<InputMatcher> |  |
| normalizerModel | JObject |  |
| checkSelectedFeatures | void |  |
| createEvaluationTaskMySqlModel | TaskMySqlModel |  |
| findComponentTaskId | String |  |
| getMyDataSetConfig | DataIOComponent.DataSetItem |  |
| getAllResult | List<TaskResultMySqlModel> |  |
| outputs | List<OutputItem> |  |
| findHomologousBranch | List<TaskMySqlModel> |  |
| createPsiParam | JObject |  |
| createScoreParam | JObject |  |
| isOotMode | boolean |  |




