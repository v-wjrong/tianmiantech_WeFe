# Basic Information

|      |      |
|------|------|
| Name | TableDataSetFeatureTracer |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/component/TableDataSetFeatureTracer.java |
| Package Name | com.welab.wefe.board.service.component |
| Dependencies | ['cn.hutool.core.collection.CollectionUtil', 'com.welab.wefe.board.service.dto.vo.FlowDataSetOutputModel', 'com.welab.wefe.board.service.model.FlowGraph', 'com.welab.wefe.board.service.model.FlowGraphNode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'java.util.ArrayList', 'java.util.List', 'java.util.stream.Collectors'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| TableDataSetFeatureTracer | class |  |



## Class TableDataSetFeatureTracer

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | TableDataSetFeatureTracer |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| endNodeId | String |  |
| result = new ArrayList<>() | List<FlowDataSetOutputModel> |  |
| pathList = new ArrayList<>() | List<List<String>> |  |
| graph | FlowGraph |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| putTableDataSet | void |  |
| getDateSet | FlowDataSetOutputModel |  |
| rollUp | void |  |
| check | void |  |




