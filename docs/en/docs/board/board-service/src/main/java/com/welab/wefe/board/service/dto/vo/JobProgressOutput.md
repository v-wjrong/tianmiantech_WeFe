# Basic Information

|      |      |
|------|------|
| Name | JobProgressOutput |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/dto/vo/JobProgressOutput.java |
| Package Name | com.welab.wefe.board.service.dto.vo |
| Dependencies | ['com.welab.wefe.board.service.database.entity.job.JobMySqlModel', 'com.welab.wefe.board.service.database.entity.job.TaskMySqlModel', 'com.welab.wefe.board.service.dto.entity.job.JobMemberOutputModel', 'com.welab.wefe.board.service.service.CacheObjects', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'com.welab.wefe.common.wefe.enums.JobStatus', 'com.welab.wefe.common.wefe.enums.TaskStatus'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| JobProgressOutput | class |  |



## Class JobProgressOutput

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | JobProgressOutput |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
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

### Method List

| Name  | Type  | Description |
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




