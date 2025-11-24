# 基础信息

|      |      |
|------|------|
| 名称 | FusionTaskMySqlModel |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/database/entity/fusion/FusionTaskMySqlModel.java |
| 包名 | com.welab.wefe.board.service.database.entity.fusion |
| 依赖项 | ['com.welab.wefe.board.service.database.entity.base.AbstractBaseMySqlModel', 'com.welab.wefe.common.wefe.enums.DataResourceType', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'com.welab.wefe.fusion.core.enums.AlgorithmType', 'com.welab.wefe.fusion.core.enums.FusionTaskStatus', 'com.welab.wefe.fusion.core.enums.PSIActuatorRole', 'javax.persistence.Column', 'javax.persistence.Entity', 'javax.persistence.EnumType', 'javax.persistence.Enumerated'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| FusionTaskMySqlModel | class |  |



## 类 FusionTaskMySqlModel

|      |      |
|------|------|
| 访问范围 | @Entity(name = "fusion_task");public |
| 类型 | class |
| 名称 | FusionTaskMySqlModel |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
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

### 方法列表

| 名称  | 类型  | 说明 |
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




