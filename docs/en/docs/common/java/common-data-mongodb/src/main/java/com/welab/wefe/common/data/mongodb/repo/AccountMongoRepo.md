# Basic Information

|      |      |
|------|------|
| Name | AccountMongoRepo |
| Language | .java |
| Code Path | WeFe/common/java/common-data-mongodb/src/main/java/com/welab/wefe/common/data/mongodb/repo/AccountMongoRepo.java |
| Package Name | com.welab.wefe.common.data.mongodb.repo |
| Dependencies | ['com.alibaba.fastjson.JSONArray', 'com.mongodb.client.result.UpdateResult', 'com.welab.wefe.common.data.mongodb.dto.PageOutput', 'com.welab.wefe.common.data.mongodb.entity.manager.Account', 'com.welab.wefe.common.data.mongodb.util.QueryBuilder', 'com.welab.wefe.common.data.mongodb.util.UpdateBuilder', 'com.welab.wefe.common.util.DateUtil', 'com.welab.wefe.common.wefe.enums.AuditStatus', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.data.mongodb.core.MongoTemplate', 'org.springframework.data.mongodb.core.query.Query', 'org.springframework.data.mongodb.core.query.Update', 'org.springframework.stereotype.Repository', 'java.util.Date', 'java.util.List'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| AccountMongoRepo | class |  |



## Class AccountMongoRepo

|      |      |
|------|------|
| Access Modifier | @Repository;public |
| Type | class |
| Name | AccountMongoRepo |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| mongoManagerTemplate | MongoTemplate |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| updateLastActionTime | void |  |
| findByAccountId | Account |  |
| disableAccountWithoutAction90Days | long |  |
| findAll | List<Account> |  |
| findByPhoneNumber | Account |  |
| getMongoTemplate | MongoTemplate |  |
| findList | PageOutput<Account> |  |
| count | long |  |
| checkAccountIsExist | boolean |  |
| find | Account |  |
| getSuperAdmin | Account |  |
| cancelAccountWithoutAction180Days | long |  |
| update | void |  |




