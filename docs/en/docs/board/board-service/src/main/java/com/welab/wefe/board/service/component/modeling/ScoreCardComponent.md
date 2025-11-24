# Basic Information

|      |      |
|------|------|
| Name | ScoreCardComponent |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/component/modeling/ScoreCardComponent.java |
| Package Name | com.welab.wefe.board.service.component.modeling |
| Dependencies | ['com.alibaba.fastjson.JSONObject', 'com.welab.wefe.board.service.component.base.io.IODataType', 'com.welab.wefe.board.service.component.base.io.InputMatcher', 'com.welab.wefe.board.service.component.base.io.Names', 'com.welab.wefe.board.service.component.base.io.OutputItem', 'com.welab.wefe.board.service.database.entity.job.TaskMySqlModel', 'com.welab.wefe.board.service.database.entity.job.TaskResultMySqlModel', 'com.welab.wefe.board.service.exception.FlowNodeException', 'com.welab.wefe.board.service.model.FlowGraph', 'com.welab.wefe.board.service.model.FlowGraphNode', 'com.welab.wefe.board.service.model.JobBuilder', 'com.welab.wefe.common.fieldvalidate.AbstractCheckModel', 'com.welab.wefe.common.fieldvalidate.annotation.Check', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.wefe.enums.ComponentType', 'com.welab.wefe.common.wefe.enums.TaskResultType', 'org.apache.commons.compress.utils.Lists', 'org.springframework.stereotype.Service', 'java.math.BigDecimal', 'java.util.Arrays', 'java.util.List'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| ScoreCardComponent | class |  |



## Class ScoreCardComponent

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | ScoreCardComponent |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|

### Method List

| Name  | Type  | Description |
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




