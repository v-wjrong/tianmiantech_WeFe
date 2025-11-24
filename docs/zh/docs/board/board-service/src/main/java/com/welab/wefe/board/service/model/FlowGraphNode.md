# 基础信息

|      |      |
|------|------|
| 名称 | FlowGraphNode |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/model/FlowGraphNode.java |
| 包名 | com.welab.wefe.board.service.model |
| 依赖项 | ['cn.hutool.core.collection.CollectionUtil', 'com.welab.wefe.board.service.component.Components', 'com.welab.wefe.board.service.component.base.AbstractComponent', 'com.welab.wefe.board.service.database.entity.job.JobMySqlModel', 'com.welab.wefe.board.service.database.entity.job.ProjectFlowNodeMySqlModel', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.fieldvalidate.AbstractCheckModel', 'com.welab.wefe.common.wefe.enums.ComponentType', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'org.apache.commons.lang3.StringUtils', 'java.util.ArrayList', 'java.util.List', 'java.util.stream.Collectors'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| FlowGraphNode | class |  |



## 类 FlowGraphNode

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | FlowGraphNode |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| paramsModel | AbstractCheckModel |  |
| parents = new ArrayList<>() | List<FlowGraphNode> |  |
| taskName | String |  |
| position | Integer |  |
| children = new ArrayList<>() | List<FlowGraphNode> |  |
| hasCacheResult | Boolean |  |
| deep | Integer |  |
| leafNode = false | boolean |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getParents | List<FlowGraphNode> |  |
| getDeep | Integer |  |
| setDeep | void |  |
| setTaskName | void |  |
| getComponent | AbstractComponent<?> |  |
| getHasCacheResult | Boolean |  |
| createTaskName | String |  |
| createTaskId | String |  |
| createTaskId | String |  |
| createParentTaskIds | String |  |
| createTaskId | String |  |
| getPosition | Integer |  |
| setParents | void |  |
| createTaskId | String |  |
| getTaskName | String |  |
| getParamsModel | T |  |
| setHasCacheResult | void |  |
| setPosition | void |  |
| createParentTaskIds | String |  |
| getChildren | List<FlowGraphNode> |  |
| setChildren | void |  |
| isLeafNode | boolean |  |
| setLeafNode | void |  |




