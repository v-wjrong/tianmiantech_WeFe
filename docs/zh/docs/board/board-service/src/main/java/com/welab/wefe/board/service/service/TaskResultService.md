# 基础信息

|      |      |
|------|------|
| 名称 | TaskResultService |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/TaskResultService.java |
| 包名 | com.welab.wefe.board.service.service |
| 依赖项 | ['com.alibaba.fastjson.JSON', 'com.alibaba.fastjson.JSONObject', 'com.welab.wefe.board.service.api.data_resource.table_data_set.DetailApi', 'com.welab.wefe.board.service.api.project.job.task.GetFeatureApi', 'com.welab.wefe.board.service.component.DataIOComponent', 'com.welab.wefe.board.service.component.base.io.Names', 'com.welab.wefe.board.service.component.base.io.NodeOutputItem', 'com.welab.wefe.board.service.component.feature.FeatureSelectionComponent', 'com.welab.wefe.board.service.component.feature.HorzOneHotComponent', 'com.welab.wefe.board.service.component.feature.HorzOneHotComponent.Params.MemberInfoModel', 'com.welab.wefe.board.service.database.entity.data_resource.TableDataSetMysqlModel', 'com.welab.wefe.board.service.database.entity.job.TaskMySqlModel', 'com.welab.wefe.board.service.database.entity.job.TaskResultMySqlModel', 'com.welab.wefe.board.service.database.repository.TaskRepository', 'com.welab.wefe.board.service.database.repository.TaskResultRepository', 'com.welab.wefe.board.service.dto.entity.MemberFeatureInfoModel', 'com.welab.wefe.board.service.dto.entity.data_resource.output.TableDataSetOutputModel', 'com.welab.wefe.board.service.exception.FlowNodeException', 'com.welab.wefe.board.service.exception.MemberGatewayException', 'com.welab.wefe.board.service.model.FlowGraph', 'com.welab.wefe.board.service.model.FlowGraphNode', 'com.welab.wefe.board.service.service.data_resource.table_data_set.TableDataSetService', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.data.mysql.Where', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.web.util.CurrentAccountUtil', 'com.welab.wefe.common.wefe.enums.ComponentType', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'com.welab.wefe.common.wefe.enums.TaskResultType', 'org.apache.commons.collections.CollectionUtils', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.data.jpa.domain.Specification', 'org.springframework.stereotype.Service', 'java.util.ArrayList', 'java.util.Arrays', 'java.util.List', 'java.util.Set'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| TaskResultService | class |  |



## 类 TaskResultService

|      |      |
|------|------|
| 访问范围 | @Service;public |
| 类型 | class |
| 名称 | TaskResultService |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| gatewayService | GatewayService |  |
| jobService | JobService |  |
| taskService | TaskService |  |
| projectFlowNodeService | ProjectFlowNodeService |  |
| taskResultRepository | TaskResultRepository |  |
| projectMemberService | ProjectMemberService |  |
| tableDataSetService | TableDataSetService |  |
| projectService | ProjectService |  |
| taskRepository | TaskRepository |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getDataIOFeature | List<MemberFeatureInfoModel> |  |
| getFeatureSelectFeature | List<MemberFeatureInfoModel> |  |
| findByTaskIdAndRoleNotEqualType | List<TaskResultMySqlModel> |  |
| findList | List<TaskResultMySqlModel> |  |
| findModelByJobIdAndTypeAndRole | List<TaskResultMySqlModel> |  |
| parserBinningResult | MemberFeatureInfoModel |  |
| setInfoAboutBinning | void |  |
| findOne | TaskResultMySqlModel |  |
| parseBinningResult | List<JObject> |  |
| getBinningResultFeature | List<MemberFeatureInfoModel> |  |
| setInfoAboutStatistic | void |  |
| setCvIvMissingRate | void |  |
| getOneHotFeature | List<MemberFeatureInfoModel> |  |
| listAllResult | List<TaskResultMySqlModel> |  |
| findModelByJobIdAndNodeIdAndRole | TaskResultMySqlModel |  |
| findByTaskIdAndType | TaskResultMySqlModel |  |
| getMemberFeatures | List<MemberFeatureInfoModel> |  |
| findByTaskIdAndTypeAndRole | TaskResultMySqlModel |  |
| getResultFeature | GetFeatureApi.Output |  |
| stopDeepLearningInfer | void |  |
| findByJobIdAndComponentTypeAndType | TaskResultMySqlModel |  |




