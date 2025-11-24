# Basic Information

|      |      |
|------|------|
| Name | ListFlowTableDataSetApi |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/api/project/flow/ListFlowTableDataSetApi.java |
| Package Name | com.welab.wefe.board.service.api.project.flow |
| Dependencies | ['com.welab.wefe.board.service.api.project.dataset.GetFeaturesApi', 'com.welab.wefe.board.service.component.base.dto.AbstractDataSetItem', 'com.welab.wefe.board.service.database.entity.job.ProjectFlowMySqlModel', 'com.welab.wefe.board.service.database.entity.job.ProjectFlowNodeMySqlModel', 'com.welab.wefe.board.service.dto.vo.FeatureOutput', 'com.welab.wefe.board.service.dto.vo.FlowDataSetOutputModel', 'com.welab.wefe.board.service.service.DataSetColumnService', 'com.welab.wefe.board.service.service.ProjectFlowJobService', 'com.welab.wefe.board.service.service.ProjectFlowNodeService', 'com.welab.wefe.board.service.service.ProjectFlowService', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.fieldvalidate.annotation.Check', 'com.welab.wefe.common.web.api.base.AbstractApi', 'com.welab.wefe.common.web.api.base.Api', 'com.welab.wefe.common.web.dto.AbstractApiInput', 'com.welab.wefe.common.web.dto.AbstractApiOutput', 'com.welab.wefe.common.web.dto.ApiResult', 'org.apache.commons.collections4.CollectionUtils', 'org.springframework.beans.factory.annotation.Autowired', 'java.io.IOException', 'java.util.ArrayList', 'java.util.List'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| ListFlowTableDataSetApi | class |  |



## Class ListFlowTableDataSetApi

|      |      |
|------|------|
| Access Modifier | @Api(path = "project/flow/table_data_set/list", name = "获取当前流程使用到的数据集列表");public |
| Type | class |
| Name | ListFlowTableDataSetApi |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| dataSetColumnService | DataSetColumnService |  |
| projectFlowJobService | ProjectFlowJobService |  |
| projectFlowNodeService | ProjectFlowNodeService |  |
| projectFlowService | ProjectFlowService |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| handle | ApiResult<Output> |  |




