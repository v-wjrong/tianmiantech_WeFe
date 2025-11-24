# 基础信息

|      |      |
|------|------|
| 名称 | ScoreCardComponent |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/component/modeling/ScoreCardComponent.java |
| 包名 | com.welab.wefe.board.service.component.modeling |
| 依赖项 | ['com.alibaba.fastjson.JSONObject', 'com.welab.wefe.board.service.component.base.io.IODataType', 'com.welab.wefe.board.service.component.base.io.InputMatcher', 'com.welab.wefe.board.service.component.base.io.Names', 'com.welab.wefe.board.service.component.base.io.OutputItem', 'com.welab.wefe.board.service.database.entity.job.TaskMySqlModel', 'com.welab.wefe.board.service.database.entity.job.TaskResultMySqlModel', 'com.welab.wefe.board.service.exception.FlowNodeException', 'com.welab.wefe.board.service.model.FlowGraph', 'com.welab.wefe.board.service.model.FlowGraphNode', 'com.welab.wefe.board.service.model.JobBuilder', 'com.welab.wefe.common.fieldvalidate.AbstractCheckModel', 'com.welab.wefe.common.fieldvalidate.annotation.Check', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.wefe.enums.ComponentType', 'com.welab.wefe.common.wefe.enums.TaskResultType', 'org.apache.commons.compress.utils.Lists', 'org.springframework.stereotype.Service', 'java.math.BigDecimal', 'java.util.Arrays', 'java.util.List'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| ScoreCardComponent | class |  |



## 类 ScoreCardComponent

|      |      |
|------|------|
| 访问范围 | @Service;public |
| 类型 | class |
| 名称 | ScoreCardComponent |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getAllResult | List<TaskResultMySqlModel> |  |
| getModelResult | JObject |  |
| takeSuffix | String |  |
| extractWoeArray | List<Double> |  |
| extractSplitPoints | List<Double> |  |
| checkBeforeBuildTask | void |  |
| getScoreCardResult | String |  |
| extractBScore | double |  |
| createTaskParams | JSONObject |  |
| getBinningSplit | String |  |
| getBinningResult | JObject |  |
| scoreCardKey | String |  |
| getResult | TaskResultMySqlModel |  |
| taskType | ComponentType |  |
| precisionProcessByDouble | String |  |
| inputs | List<InputMatcher> |  |
| outputs | List<OutputItem> |  |




