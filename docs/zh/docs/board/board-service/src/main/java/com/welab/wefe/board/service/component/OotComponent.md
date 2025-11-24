# 基础信息

|      |      |
|------|------|
| 名称 | OotComponent |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/component/OotComponent.java |
| 包名 | com.welab.wefe.board.service.component |
| 依赖项 | ['com.alibaba.fastjson.JSON', 'com.alibaba.fastjson.JSONObject', 'com.welab.wefe.board.service.api.project.flow.QueryDataIoTaskConfigApi', 'com.welab.wefe.board.service.api.project.member.ListInProjectApi', 'com.welab.wefe.board.service.component.base.AbstractComponent', 'com.welab.wefe.board.service.component.base.dto.AbstractDataIOParam', 'com.welab.wefe.board.service.component.base.io.IODataType', 'com.welab.wefe.board.service.component.base.io.InputMatcher', 'com.welab.wefe.board.service.component.base.io.Names', 'com.welab.wefe.board.service.component.base.io.OutputItem', 'com.welab.wefe.board.service.constant.Config', 'com.welab.wefe.board.service.database.entity.data_resource.TableDataSetMysqlModel', 'com.welab.wefe.board.service.database.entity.job', 'com.welab.wefe.board.service.dto.kernel.machine_learning.TaskConfig', 'com.welab.wefe.board.service.exception.FlowNodeException', 'com.welab.wefe.board.service.model.FlowGraph', 'com.welab.wefe.board.service.model.FlowGraphNode', 'com.welab.wefe.board.service.model.JobBuilder', 'com.welab.wefe.board.service.service', 'com.welab.wefe.board.service.service.data_resource.table_data_set.TableDataSetService', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.wefe.enums.ComponentType', 'com.welab.wefe.common.wefe.enums.FederatedLearningType', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'com.welab.wefe.common.wefe.enums.TaskResultType', 'org.apache.commons.collections4.CollectionUtils', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.stereotype.Service', 'java.util', 'java.util.stream.Collectors'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| OotComponent | class |  |



## 类 OotComponent

|      |      |
|------|------|
| 访问范围 | @Service;public |
| 类型 | class |
| 名称 | OotComponent |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| projectFlowNodeService | ProjectFlowNodeService |  |
| config | Config |  |
| gatewayService | GatewayService |  |
| TEMP_UNSUPPORTED_COMPONENT_TYPE_LIST = Arrays.asList(ComponentType.MixLR,            ComponentType.MixSecureBoost, ComponentType.HorzNN, ComponentType.VertNN) | List<ComponentType> |  |
| tableDataSetService | TableDataSetService |  |
| EXCLUDE_COMPONENT_TYPE_LIST = Arrays.asList(ComponentType.FeatureStatistic,            ComponentType.FeatureCalculation, ComponentType.MixStatistic,            ComponentType.Segment, ComponentType.VertPearson, ComponentType.Oot, ComponentType.VertFeaturePSI, ComponentType.VertFilter, ComponentType.ScoreCard) | List<ComponentType> |  |
| projectMemberService | ProjectMemberService |  |
| taskService | TaskService |  |

### 方法列表

| 名称  | 类型  | 说明 |
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




