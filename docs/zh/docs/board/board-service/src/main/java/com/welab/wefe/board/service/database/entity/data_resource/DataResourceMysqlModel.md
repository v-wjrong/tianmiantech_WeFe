# 基础信息

|      |      |
|------|------|
| 名称 | DataResourceMysqlModel |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/database/entity/data_resource/DataResourceMysqlModel.java |
| 包名 | com.welab.wefe.board.service.database.entity.data_resource |
| 依赖项 | ['com.alibaba.fastjson.JSONObject', 'com.alibaba.fastjson.annotation.JSONField', 'com.vladmihalcea.hibernate.type.json.JsonStringType', 'com.welab.wefe.board.service.database.entity.base.AbstractBaseMySqlModel', 'com.welab.wefe.common.wefe.enums.ComponentType', 'com.welab.wefe.common.wefe.enums.DataResourcePublicLevel', 'com.welab.wefe.common.wefe.enums.DataResourceStorageServiceType', 'com.welab.wefe.common.wefe.enums.DataResourceType', 'org.hibernate.annotations.Type', 'org.hibernate.annotations.TypeDef', 'javax.persistence', 'java.io.File', 'java.nio.file.Path', 'java.nio.file.Paths'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| DataResourceMysqlModel | class |  |



## 类 DataResourceMysqlModel

|      |      |
|------|------|
| 访问范围 | @Entity(name = "data_resource");@Table(name = "data_resource");@Inheritance(strategy = InheritanceType.JOINED);@TypeDef(name = "json", typeClass = JsonStringType.class);public |
| 类型 | class |
| 名称 | DataResourceMysqlModel |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| statisticalInformation | JSONObject |  |
| description | String |  |
| dataResourceType | DataResourceType |  |
| storageResourceName | String |  |
| derivedFromTaskId | String |  |
| derivedResource | boolean |  |
| usageCountInMember | int |  |
| publicMemberList | String |  |
| storageNamespace | String |  |
| publicLevel | DataResourcePublicLevel |  |
| storageType | DataResourceStorageServiceType |  |
| usageCountInJob | int |  |
| derivedFromJobId | String |  |
| usageCountInProject | int |  |
| name | String |  |
| totalDataCount | long |  |
| tags | String |  |
| derivedFromFlowId | String |  |
| derivedFrom | ComponentType |  |
| usageCountInFlow | int |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| setDataResourceType | void |  |
| setTotalDataCount | void |  |
| setDescription | void |  |
| getDerivedFromFlowId | String |  |
| setDerivedFromFlowId | void |  |
| getDerivedFromJobId | String |  |
| setDerivedFromJobId | void |  |
| getDerivedFromTaskId | String |  |
| setDerivedFromTaskId | void |  |
| getStatisticalInformation | JSONObject |  |
| setStatisticalInformation | void |  |
| getStorageType | DataResourceStorageServiceType |  |
| getStorageResourceName | String |  |
| isDerivedResource | boolean |  |
| getDataResourceType | DataResourceType |  |
| setPublicLevel | void |  |
| getTotalDataCount | Long |  |
| getUsageCountInFlow | int |  |
| setStorageNamespace | void |  |
| getTags | String |  |
| setUsageCountInMember | void |  |
| setUsageCountInJob | void |  |
| dir | Path |  |
| setDerivedFrom | void |  |
| setTags | void |  |
| setName | void |  |
| getUsageCountInProject | int |  |
| getPublicMemberList | String |  |
| file | File |  |
| getPublicLevel | DataResourcePublicLevel |  |
| getStorageNamespace | String |  |
| getUsageCountInMember | int |  |
| getUsageCountInJob | int |  |
| setUsageCountInFlow | void |  |
| getName | String |  |
| getDerivedFrom | ComponentType |  |
| getDescription | String |  |
| setPublicMemberList | void |  |
| setStorageType | void |  |
| setUsageCountInProject | void |  |
| setDerivedResource | void |  |
| setStorageResourceName | void |  |




