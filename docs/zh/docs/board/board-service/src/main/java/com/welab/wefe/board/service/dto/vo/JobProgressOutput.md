# 基础信息

|      |      |
|------|------|
| 名称 | JobProgressOutput |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/dto/vo/JobProgressOutput.java |
| 包名 | com.welab.wefe.board.service.dto.vo |
| 依赖项 | ['com.welab.wefe.board.service.database.entity.job.JobMySqlModel', 'com.welab.wefe.board.service.database.entity.job.TaskMySqlModel', 'com.welab.wefe.board.service.dto.entity.job.JobMemberOutputModel', 'com.welab.wefe.board.service.service.CacheObjects', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'com.welab.wefe.common.wefe.enums.JobStatus', 'com.welab.wefe.common.wefe.enums.TaskStatus'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| JobProgressOutput | class |  |



## 类 JobProgressOutput

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | JobProgressOutput |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| jobRole | JobMemberRole |  |
| getProgressSuccess | boolean |  |
| jobStatus | JobStatus |  |
| progress | int |  |
| nodeId | String |  |
| message | String |  |
| memberId | String |  |
| taskStatus | TaskStatus |  |
| taskId | String |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getJobRole | JobMemberRole |  |
| setJobRole | void |  |
| setGetProgressSuccess | void |  |
| getMessage | String |  |
| setMessage | void |  |
| fail | JobProgressOutput |  |
| setNodeId | void |  |
| setJobStatus | void |  |
| setProgress | void |  |
| getProgress | int |  |
| getMemberId | String |  |
| setMemberId | void |  |
| setTaskStatus | void |  |
| getMemberName | String |  |
| setTaskId | void |  |
| getTaskId | String |  |
| getJobStatus | JobStatus |  |
| isGetProgressSuccess | boolean |  |
| getTaskStatus | TaskStatus |  |
| success | JobProgressOutput |  |
| getNodeId | String |  |




