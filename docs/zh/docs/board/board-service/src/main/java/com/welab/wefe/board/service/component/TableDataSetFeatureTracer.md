# 基础信息

|      |      |
|------|------|
| 名称 | TableDataSetFeatureTracer |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/component/TableDataSetFeatureTracer.java |
| 包名 | com.welab.wefe.board.service.component |
| 依赖项 | ['cn.hutool.core.collection.CollectionUtil', 'com.welab.wefe.board.service.dto.vo.FlowDataSetOutputModel', 'com.welab.wefe.board.service.model.FlowGraph', 'com.welab.wefe.board.service.model.FlowGraphNode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'java.util.ArrayList', 'java.util.List', 'java.util.stream.Collectors'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| TableDataSetFeatureTracer | class |  |



## 类 TableDataSetFeatureTracer

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | TableDataSetFeatureTracer |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| endNodeId | String |  |
| result = new ArrayList<>() | List<FlowDataSetOutputModel> |  |
| pathList = new ArrayList<>() | List<List<String>> |  |
| graph | FlowGraph |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| putTableDataSet | void |  |
| getDateSet | FlowDataSetOutputModel |  |
| rollUp | void |  |
| check | void |  |




