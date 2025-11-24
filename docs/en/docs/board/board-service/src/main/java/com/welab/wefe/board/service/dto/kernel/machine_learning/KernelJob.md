# Basic Information

|      |      |
|------|------|
| Name | KernelJob |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/dto/kernel/machine_learning/KernelJob.java |
| Package Name | com.welab.wefe.board.service.dto.kernel.machine_learning |
| Dependencies | ['com.alibaba.fastjson.JSONObject', 'com.welab.wefe.board.service.dto.kernel.Member', 'com.welab.wefe.common.fieldvalidate.annotation.Check', 'com.welab.wefe.common.wefe.enums.FederatedLearningModel', 'com.welab.wefe.common.wefe.enums.FederatedLearningType', 'java.util.List'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| KernelJob | class |  |



## Class KernelJob

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | KernelJob |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| env | Env |  |
| members | List<Member> |  |
| federatedLearningMode | FederatedLearningModel |  |
| federatedLearningType | FederatedLearningType |  |
| mixPromoterMemberId | String |  |
| dataSets | List<JobDataSet> |  |
| project | Project |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| setFederatedLearningType | void |  |
| setMixPromoterMemberId | void |  |
| getMembers | List<Member> |  |
| setProject | void |  |
| getEnv | Env |  |
| setDataSets | void |  |
| setEnv | void |  |
| getProject | Project |  |
| toJson | JSONObject |  |
| getFederatedLearningType | FederatedLearningType |  |
| getDataSets | List<JobDataSet> |  |
| getMixPromoterMemberId | String |  |
| setMembers | void |  |
| getFederatedLearningMode | FederatedLearningModel |  |
| setFederatedLearningMode | void |  |




