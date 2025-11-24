# Basic Information

|      |      |
|------|------|
| Name | AbstractComponent |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/component/base/AbstractComponent.java |
| Package Name | com.welab.wefe.board.service.component.base |
| Dependencies | ['com.alibaba.fastjson.JSON', 'com.alibaba.fastjson.JSONObject', 'com.alibaba.fastjson.TypeReference', 'com.welab.wefe.board.service.component.Components', 'com.welab.wefe.board.service.component.DataIOComponent', 'com.welab.wefe.board.service.component.OotComponent', 'com.welab.wefe.board.service.component.base.io', 'com.welab.wefe.board.service.database.entity.data_resource.TableDataSetMysqlModel', 'com.welab.wefe.board.service.database.entity.job.ProjectMySqlModel', 'com.welab.wefe.board.service.database.entity.job.TaskMySqlModel', 'com.welab.wefe.board.service.database.entity.job.TaskResultMySqlModel', 'com.welab.wefe.board.service.database.repository.TaskRepository', 'com.welab.wefe.board.service.dto.entity.job.TaskResultOutputModel', 'com.welab.wefe.board.service.dto.kernel.Member', 'com.welab.wefe.board.service.dto.kernel.machine_learning.KernelTask', 'com.welab.wefe.board.service.dto.kernel.machine_learning.TaskConfig', 'com.welab.wefe.board.service.exception.FlowNodeException', 'com.welab.wefe.board.service.model.FlowGraph', 'com.welab.wefe.board.service.model.FlowGraphNode', 'com.welab.wefe.board.service.model.JobBuilder', 'com.welab.wefe.board.service.service.CacheObjects', 'com.welab.wefe.board.service.service.JobService', 'com.welab.wefe.board.service.service.TaskResultService', 'com.welab.wefe.board.service.service.globalconfig.GlobalConfigService', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.fieldvalidate.AbstractCheckModel', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.web.util.ModelMapper', 'com.welab.wefe.common.wefe.enums.ComponentType', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'com.welab.wefe.common.wefe.enums.ProjectType', 'com.welab.wefe.common.wefe.enums.TaskStatus', 'org.apache.commons.collections.CollectionUtils', 'org.apache.commons.lang3.StringUtils', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.stereotype.Service', 'java.lang.reflect.ParameterizedType', 'java.lang.reflect.Type', 'java.util', 'java.util.function.Function', 'java.util.stream.Collectors'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| AbstractComponent | class |  |



## Class AbstractComponent

|      |      |
|------|------|
| Access Modifier | @Service;public abstract |
| Type | class |
| Name | AbstractComponent |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| LOG = LoggerFactory.getLogger(this.getClass()) | Logger |  |
| taskRepository | TaskRepository |  |
| jobService | JobService |  |
| taskResultService | TaskResultService |  |
| globalConfigService | GlobalConfigService |  |
| MODEL_COMPONENT_TYPE_LIST = Arrays.asList(            ComponentType.HorzLR,            ComponentType.VertLR,            ComponentType.HorzSecureBoost,            ComponentType.VertSecureBoost,            ComponentType.MixLR,            ComponentType.MixSecureBoost,            ComponentType.HorzNN,            ComponentType.VertNN    ) | List<ComponentType> |  |
| DATA_IO_COMPONENT_TYPE_LIST = Arrays.asList(            ComponentType.DataIO,            ComponentType.HorzLRValidationDataSetLoader,            ComponentType.VertLRValidationDataSetLoader,            ComponentType.HorzXGBoostValidationDataSetLoader,            ComponentType.VertXGBoostValidationDataSetLoader    ) | List<ComponentType> |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| canSelectFeatures | boolean |  |
| deserializationParam | T |  |
| getTaskAllResult | List<TaskResultOutputModel> |  |
| getTaskMembers | KernelTask |  |
| getInputs | Map<String, Object> |  |
| findTaskFromPretasks | TaskMySqlModel |  |
| getOutputs | Map<String, Object> |  |
| getMixTaskMembers | List<KernelTask> |  |
| hasParams | boolean |  |
| getTaskResult | TaskResultOutputModel |  |
| parentHasIntersectedDataSet | boolean |  |
| buildMixTask | List<TaskMySqlModel> |  |
| getParamsClass | Class<T> |  |
| findMyData | T |  |
| findInputNodes | List<NodeOutputItem> |  |
| needIntersectedDataSetBeforeMe | boolean |  |
| getCount | int |  |
| generateInput | Map<String, Object> |  |
| stopCreateTask | boolean |  |
| buildTask | TaskMySqlModel |  |
| checkBeforeBuildTask | void |  |
| createTaskParams | JSONObject |  |
| taskType | ComponentType |  |
| getAllResult | List<TaskResultMySqlModel> |  |
| getResult | TaskResultMySqlModel |  |
| inputs | List<InputMatcher> |  |
| outputs | List<OutputItem> |  |




