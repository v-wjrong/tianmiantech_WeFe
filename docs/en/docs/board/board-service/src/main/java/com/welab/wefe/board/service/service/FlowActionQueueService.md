# Basic Information

|      |      |
|------|------|
| Name | FlowActionQueueService |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/FlowActionQueueService.java |
| Package Name | com.welab.wefe.board.service.service |
| Dependencies | ['com.welab.wefe.board.service.database.entity.flow.FlowActionQueueMySqlModel', 'com.welab.wefe.board.service.database.entity.job.JobMySqlModel', 'com.welab.wefe.board.service.database.repository.FlowActionQueueRepository', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.web.dto.AbstractApiInput', 'com.welab.wefe.common.wefe.enums.FlowActionType', 'com.welab.wefe.common.wefe.enums.ProducerType', 'com.welab.wefe.common.wefe.enums.ProjectType', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.stereotype.Service'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| FlowActionQueueService | class |  |



## Class FlowActionQueueService

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | FlowActionQueueService |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| flowActionQueueRepository | FlowActionQueueRepository |  |
| jobService | JobService |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| runJob | void |  |
| notifyFlow | void |  |
| notifyFlow | void |  |
| stopJob | void |  |




