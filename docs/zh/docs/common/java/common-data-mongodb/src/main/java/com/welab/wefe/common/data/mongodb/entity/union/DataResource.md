# 基础信息

|      |      |
|------|------|
| 名称 | DataResource |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-data-mongodb/src/main/java/com/welab/wefe/common/data/mongodb/entity/union/DataResource.java |
| 包名 | com.welab.wefe.common.data.mongodb.entity.union |
| 依赖项 | ['com.welab.wefe.common.data.mongodb.constant.MongodbTable', 'com.welab.wefe.common.data.mongodb.entity.base.AbstractBlockChainBusinessModel', 'com.welab.wefe.common.data.mongodb.entity.union.ext.DataResourceExtJSON', 'com.welab.wefe.common.wefe.enums.DataResourceType', 'org.springframework.data.mongodb.core.mapping.Document'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| DataResource | class |  |



## 类 DataResource

|      |      |
|------|------|
| 访问范围 | @Document(collection = MongodbTable.Union.DATA_RESOURCE);public |
| 类型 | class |
| 名称 | DataResource |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| tags | String |  |
| dataResourceId | String |  |
| description | String |  |
| memberId | String |  |
| extJson = new DataResourceExtJSON() | DataResourceExtJSON |  |
| totalDataCount | String |  |
| usageCountInJob | String |  |
| enable | String |  |
| publicLevel | String |  |
| usageCountInFlow | String |  |
| publicMemberList | String |  |
| usageCountInProject | String |  |
| name | String |  |
| dataResourceType | DataResourceType |  |
| usageCountInMember | String |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getUsageCountInFlow | String |  |
| setExtJson | void |  |
| getMemberId | String |  |
| getUsageCountInJob | String |  |
| setUsageCountInJob | void |  |
| setDataResourceId | void |  |
| getUsageCountInMember | String |  |
| getPublicLevel | String |  |
| setUsageCountInFlow | void |  |
| setName | void |  |
| getDataResourceId | String |  |
| setUsageCountInMember | void |  |
| getTags | String |  |
| setUsageCountInProject | void |  |
| getDescription | String |  |
| setPublicLevel | void |  |
| setTotalDataCount | void |  |
| getExtJson | DataResourceExtJSON |  |
| setDataResourceType | void |  |
| setDescription | void |  |
| setEnable | void |  |
| setMemberId | void |  |
| getPublicMemberList | String |  |
| getTotalDataCount | String |  |
| getDataResourceType | DataResourceType |  |
| setTags | void |  |
| getEnable | String |  |
| getUsageCountInProject | String |  |
| setPublicMemberList | void |  |
| getName | String |  |




