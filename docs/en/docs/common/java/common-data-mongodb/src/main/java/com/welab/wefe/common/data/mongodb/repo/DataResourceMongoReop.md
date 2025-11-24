# Basic Information

|      |      |
|------|------|
| Name | DataResourceMongoReop |
| Language | .java |
| Code Path | WeFe/common/java/common-data-mongodb/src/main/java/com/welab/wefe/common/data/mongodb/repo/DataResourceMongoReop.java |
| Package Name | com.welab.wefe.common.data.mongodb.repo |
| Dependencies | ['com.welab.wefe.common.data.mongodb.constant.MongodbTable', 'com.welab.wefe.common.data.mongodb.dto.PageOutput', 'com.welab.wefe.common.data.mongodb.dto.dataresource.DataResourceQueryInput', 'com.welab.wefe.common.data.mongodb.dto.dataresource.DataResourceQueryOutput', 'com.welab.wefe.common.data.mongodb.entity.union.DataResource', 'com.welab.wefe.common.data.mongodb.util.AddFieldsOperation', 'com.welab.wefe.common.data.mongodb.util.QueryBuilder', 'com.welab.wefe.common.data.mongodb.util.UpdateBuilder', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.wefe.enums.DataResourceType', 'org.apache.commons.collections4.CollectionUtils', 'org.apache.commons.lang3.StringUtils', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.data.domain.Sort', 'org.springframework.data.mongodb.core.MongoTemplate', 'org.springframework.data.mongodb.core.aggregation', 'org.springframework.data.mongodb.core.query.Criteria', 'org.springframework.data.mongodb.core.query.Query', 'org.springframework.data.mongodb.core.query.Update', 'org.springframework.stereotype.Repository', 'java.util', 'java.util.stream.Collectors'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| DataResourceMongoReop | class |  |



## Class DataResourceMongoReop

|      |      |
|------|------|
| Access Modifier | @Repository;public |
| Type | class |
| Name | DataResourceMongoReop |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| mongoUnionTemplate | MongoTemplate |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| find | PageOutput<DataResourceQueryOutput> |  |
| deleteByDataResourceId | void |  |
| findByDataResourceId | DataResource |  |
| upsert | void |  |
| buildCurMemberCanSeeMatchOperations | List<MatchOperation> |  |
| findByDataResourceType | List<String> |  |
| buildMatchOperations | List<MatchOperation> |  |
| getMongoTemplate | MongoTemplate |  |
| getTableName | String |  |
| findOneByDataResourceId | DataResourceQueryOutput |  |
| buildUnwindOperations | List<UnwindOperation> |  |
| existsByDataResourceId | boolean |  |
| find | DataResource |  |
| buildLookupOperations | List<LookupOperation> |  |
| findOneByDataResourceId | PageOutput<DataResourceQueryOutput> |  |
| findAll | PageOutput<DataResourceQueryOutput> |  |




