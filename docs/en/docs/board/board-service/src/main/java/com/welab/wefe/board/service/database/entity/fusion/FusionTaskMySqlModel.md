# Basic Information

|      |      |
|------|------|
| Name | FusionTaskMySqlModel |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/database/entity/fusion/FusionTaskMySqlModel.java |
| Package Name | com.welab.wefe.board.service.database.entity.fusion |
| Dependencies | ['com.welab.wefe.board.service.database.entity.base.AbstractBaseMySqlModel', 'com.welab.wefe.common.wefe.enums.DataResourceType', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'com.welab.wefe.fusion.core.enums.AlgorithmType', 'com.welab.wefe.fusion.core.enums.FusionTaskStatus', 'com.welab.wefe.fusion.core.enums.PSIActuatorRole', 'javax.persistence.Column', 'javax.persistence.Entity', 'javax.persistence.EnumType', 'javax.persistence.Enumerated'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| FusionTaskMySqlModel | class |  |



## Class FusionTaskMySqlModel

|      |      |
|------|------|
| Access Modifier | @Entity(name = "fusion_task");public |
| Type | class |
| Name | FusionTaskMySqlModel |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| comment | String |  |
| error | String |  |
| partnerRowCount | Long |  |
| description | String |  |
| projectId | String |  |
| hashFunction | String |  |
| name | String |  |
| isTrace | boolean |  |
| fusionCount = 0L | Long |  |
| dataResourceType | DataResourceType |  |
| partnerDataResourceId | String |  |
| processedCount = 0L | Long |  |
| algorithm | AlgorithmType |  |
| partnerHashFunction | String |  |
| dstMemberId | String |  |
| myRole | JobMemberRole |  |
| status | FusionTaskStatus |  |
| rowCount | Long |  |
| dataResourceId | String |  |
| psiActuatorRole | PSIActuatorRole |  |
| businessId | String |  |
| deleted = false | boolean |  |
| spend | long |  |
| dataCount = 0L | Long |  |
| partnerDataResourceType | DataResourceType |  |
| traceColumn | String |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| setSpend | void |  |
| setComment | void |  |
| setDataResourceId | void |  |
| getAlgorithm | AlgorithmType |  |
| setProjectId | void |  |
| setPartnerRowCount | void |  |
| setMyRole | void |  |
| getProjectId | String |  |
| setStatus | void |  |
| getError | String |  |
| setRowCount | void |  |
| setTraceColumn | void |  |
| getMyRole | JobMemberRole |  |
| getPartnerDataResourceId | String |  |
| getTraceColumn | String |  |
| getDataResourceId | String |  |
| setProcessedCount | void |  |
| getDescription | String |  |
| setDataResourceType | void |  |
| setDescription | void |  |
| getRowCount | Long |  |
| setName | void |  |
| setBusinessId | void |  |
| getComment | String |  |
| setPartnerHashFunction | void |  |
| getPsiActuatorRole | PSIActuatorRole |  |
| getHashFunction | String |  |
| isDeleted | boolean |  |
| setFusionCount | void |  |
| getBusinessId | String |  |
| setError | void |  |
| setAlgorithm | void |  |
| getName | String |  |
| getProcessedCount | Long |  |
| getFusionCount | Long |  |
| getDstMemberId | String |  |
| setDataCount | void |  |
| setPartnerDataResourceType | void |  |
| getStatus | FusionTaskStatus |  |
| getPartnerHashFunction | String |  |
| setHashFunction | void |  |
| setTrace | void |  |
| setDstMemberId | void |  |
| setPartnerDataResourceId | void |  |
| getPartnerDataResourceType | DataResourceType |  |
| getPartnerRowCount | Long |  |
| getSpend | long |  |
| setPsiActuatorRole | void |  |
| getDataResourceType | DataResourceType |  |
| isTrace | boolean |  |
| getDataCount | Long |  |
| setDeleted | void |  |




