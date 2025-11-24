# 基础信息

|      |      |
|------|------|
| 名称 | DataResourceOutputModel |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/dto/entity/data_resource/output/DataResourceOutputModel.java |
| 包名 | com.welab.wefe.board.service.dto.entity.data_resource.output |
| 依赖项 | ['com.alibaba.fastjson.JSONObject', 'com.welab.wefe.board.service.dto.entity.AbstractOutputModel', 'com.welab.wefe.board.service.service.CacheObjects', 'com.welab.wefe.common.fieldvalidate.annotation.Check', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.wefe.enums.ComponentType', 'com.welab.wefe.common.wefe.enums.DataResourcePublicLevel', 'com.welab.wefe.common.wefe.enums.DataResourceStorageServiceType', 'com.welab.wefe.common.wefe.enums.DataResourceType', 'java.util.Map', 'java.util.TreeMap'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| DataResourceOutputModel | class |  |



## 类 DataResourceOutputModel

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | DataResourceOutputModel |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| description | String |  |
| dataResourceType | DataResourceType |  |
| storageResourceName | String |  |
| derivedFromTaskId | String |  |
| deleted | boolean |  |
| derivedResource | boolean |  |
| usageCountInMember | Integer |  |
| derivedFrom | ComponentType |  |
| publicMemberList | String |  |
| storageNamespace | String |  |
| publicLevel | DataResourcePublicLevel |  |
| storageType | DataResourceStorageServiceType |  |
| derivedFromJobId | String |  |
| usageCountInProject | Integer |  |
| name | String |  |
| derivedFromFlowId | String |  |
| totalDataCount | Long |  |
| tags | String |  |
| usageCountInJob | Integer |  |
| usageCountInFlow | Integer |  |
| statisticalInformation | JSONObject |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getName | String |  |
| getDerivedFromTaskId | String |  |
| setDerivedFrom | void |  |
| setStorageNamespace | void |  |
| setUsageCountInMember | void |  |
| setName | void |  |
| setStorageResourceName | void |  |
| getTags | String |  |
| getPublicLevel | DataResourcePublicLevel |  |
| setDerivedFromTaskId | void |  |
| getStorageNamespace | String |  |
| getUsageCountInMember | Integer |  |
| setDeleted | void |  |
| setTotalDataCount | void |  |
| getStorageResourceName | String |  |
| getDescription | String |  |
| getUsageCountInJob | Integer |  |
| setStorageType | void |  |
| setUsageCountInProject | void |  |
| setPublicMemberList | void |  |
| setDerivedResource | void |  |
| isDeleted | boolean |  |
| setDerivedFromFlowId | void |  |
| setDescription | void |  |
| getDerivedFromCn | String |  |
| getDataResourceId | String |  |
| setDerivedFromJobId | void |  |
| getUsageCountInFlow | Integer |  |
| getDerivedFrom | ComponentType |  |
| getTotalDataCount | Long |  |
| getStorageType | DataResourceStorageServiceType |  |
| getUsageCountInProject | Integer |  |
| setStatisticalInformation | void |  |
| getPublicMemberList | String |  |
| setUsageCountInJob | void |  |
| getPublicMemberInfoList | Map<String, String> |  |
| getDerivedFromFlowId | String |  |
| isDerivedResource | boolean |  |
| getDerivedFromJobId | String |  |
| getDataResourceType | DataResourceType |  |
| setDataResourceType | void |  |
| getStatisticalInformation | JSONObject |  |
| setPublicLevel | void |  |
| setTags | void |  |
| setUsageCountInFlow | void |  |




