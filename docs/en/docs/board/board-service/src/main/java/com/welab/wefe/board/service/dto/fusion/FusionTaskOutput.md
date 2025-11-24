# Basic Information

|      |      |
|------|------|
| Name | FusionTaskOutput |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/dto/fusion/FusionTaskOutput.java |
| Package Name | com.welab.wefe.board.service.dto.fusion |
| Dependencies | ['com.welab.wefe.board.service.dto.entity.AbstractOutputModel', 'com.welab.wefe.board.service.dto.entity.data_resource.output.BloomFilterOutputModel', 'com.welab.wefe.board.service.dto.entity.data_resource.output.TableDataSetOutputModel', 'com.welab.wefe.board.service.fusion.enums.ExportStatus', 'com.welab.wefe.common.fieldvalidate.annotation.Check', 'com.welab.wefe.common.wefe.enums.DataResourceType', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'com.welab.wefe.fusion.core.enums.AlgorithmType', 'com.welab.wefe.fusion.core.enums.FusionTaskStatus', 'com.welab.wefe.fusion.core.enums.PSIActuatorRole', 'javax.persistence.Column', 'javax.persistence.EnumType', 'javax.persistence.Enumerated', 'java.util.List'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| FusionTaskOutput | class |  |



## Class FusionTaskOutput

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | FusionTaskOutput |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| promoter | FusionMemberInfo |  |
| name | String |  |
| businessId | String |  |
| dataResourceType | DataResourceType |  |
| spend | long |  |
| isTrace | boolean |  |
| provider | FusionMemberInfo |  |
| partnerRowCount | Long |  |
| ExportStatus | ExportStatus |  |
| hashFunction | String |  |
| error | String |  |
| rowCount | Long |  |
| dataResourceId | String |  |
| traceColumn | String |  |
| psiActuatorRole | PSIActuatorRole |  |
| status | FusionTaskStatus |  |
| description | String |  |
| myRole | JobMemberRole |  |
| fusionCount | int |  |
| dstMemberId | String |  |
| dataResourceName | String |  |
| partnerHashFunction | String |  |
| partnerDataResourceId | String |  |
| algorithm | AlgorithmType |  |
| partnerDataResourceType | DataResourceType |  |
| partnerDataResourceName | String |  |
| comment | String |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| setMyRole | void |  |
| setAlgorithm | void |  |
| setDataResourceName | void |  |
| setRowCount | void |  |
| getBusinessId | String |  |
| getPartnerDataResourceName | String |  |
| setDescription | void |  |
| setDstMemberId | void |  |
| getFusionCount | int |  |
| setStatus | void |  |
| setDataResourceType | void |  |
| getComment | String |  |
| getTraceColumn | String |  |
| getDataResourceId | String |  |
| getStatus | FusionTaskStatus |  |
| getDstMemberId | String |  |
| getProvider | FusionMemberInfo |  |
| getSpend | long |  |
| setHashFunction | void |  |
| setError | void |  |
| setPromoter | void |  |
| getPartnerDataResourceId | String |  |
| setBusinessId | void |  |
| getDataResourceType | DataResourceType |  |
| getDescription | String |  |
| setName | void |  |
| setTrace | void |  |
| getPartnerDataResourceType | DataResourceType |  |
| getPromoter | FusionMemberInfo |  |
| setDataResourceId | void |  |
| setSpend | void |  |
| getPsiActuatorRole | PSIActuatorRole |  |
| isTrace | boolean |  |
| getPartnerRowCount | Long |  |
| setPartnerDataResourceType | void |  |
| setPsiActuatorRole | void |  |
| setTraceColumn | void |  |
| getName | String |  |
| getError | String |  |
| getHashFunction | String |  |
| setFusionCount | void |  |
| getAlgorithm | AlgorithmType |  |
| setPartnerRowCount | void |  |
| getDataResourceName | String |  |
| getMyRole | JobMemberRole |  |
| setPartnerDataResourceName | void |  |
| getRowCount | Long |  |
| setPartnerDataResourceId | void |  |
| setComment | void |  |
| setProvider | void |  |
| getPartnerHashFunction | String |  |
| setPartnerHashFunction | void |  |
| getExportStatus | com.welab.wefe.board.service.fusion.enums.ExportStatus |  |
| setExportStatus | void |  |




