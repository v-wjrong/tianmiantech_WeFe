# Basic Information

|      |      |
|------|------|
| Name | MemberMongoReop |
| Language | .java |
| Code Path | WeFe/common/java/common-data-mongodb/src/main/java/com/welab/wefe/common/data/mongodb/repo/MemberMongoReop.java |
| Package Name | com.welab.wefe.common.data.mongodb.repo |
| Dependencies | ['com.mongodb.client.result.UpdateResult', 'com.welab.wefe.common.data.mongodb.dto.PageOutput', 'com.welab.wefe.common.data.mongodb.entity.union.Member', 'com.welab.wefe.common.data.mongodb.entity.union.ext.MemberExtJSON', 'com.welab.wefe.common.data.mongodb.util.QueryBuilder', 'com.welab.wefe.common.data.mongodb.util.UpdateBuilder', 'org.apache.commons.lang3.StringUtils', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.data.mongodb.core.MongoTemplate', 'org.springframework.data.mongodb.core.query.Query', 'org.springframework.data.mongodb.core.query.Update', 'org.springframework.stereotype.Repository', 'java.util.ArrayList', 'java.util.List'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| MemberMongoReop | class |  |



## Class MemberMongoReop

|      |      |
|------|------|
| Access Modifier | @Repository;public |
| Type | class |
| Name | MemberMongoReop |
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
| updateExcludeLogo | boolean |  |
| existsByMemberId | boolean |  |
| getMongoTemplate | MongoTemplate |  |
| query | PageOutput<Member> |  |
| updateLogoById | boolean |  |
| updateLastActivityTimeById | boolean |  |
| query | PageOutput<Member> |  |
| find | List<Member> |  |
| updatePulicKeyById | boolean |  |
| upsert | void |  |
| deleteMemberById | boolean |  |
| findMemberId | Member |  |
| updateExcludePublicKey | boolean |  |
| updateExtJSONById | boolean |  |




