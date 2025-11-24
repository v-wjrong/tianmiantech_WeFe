# 基础信息

|      |      |
|------|------|
| 名称 | KernelJob |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/dto/kernel/machine_learning/KernelJob.java |
| 包名 | com.welab.wefe.board.service.dto.kernel.machine_learning |
| 依赖项 | ['com.alibaba.fastjson.JSONObject', 'com.welab.wefe.board.service.dto.kernel.Member', 'com.welab.wefe.common.fieldvalidate.annotation.Check', 'com.welab.wefe.common.wefe.enums.FederatedLearningModel', 'com.welab.wefe.common.wefe.enums.FederatedLearningType', 'java.util.List'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| KernelJob | class |  |



## 类 KernelJob

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | KernelJob |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| env | Env |  |
| members | List<Member> |  |
| federatedLearningMode | FederatedLearningModel |  |
| federatedLearningType | FederatedLearningType |  |
| mixPromoterMemberId | String |  |
| dataSets | List<JobDataSet> |  |
| project | Project |  |

### 方法列表

| 名称  | 类型  | 说明 |
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




