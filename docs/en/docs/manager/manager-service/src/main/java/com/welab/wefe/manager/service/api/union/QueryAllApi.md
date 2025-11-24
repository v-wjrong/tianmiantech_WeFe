# Basic Information

|      |      |
|------|------|
| Name | QueryAllApi |
| Language | .java |
| Code Path | WeFe/manager/manager-service/src/main/java/com/welab/wefe/manager/service/api/union/QueryAllApi.java |
| Package Name | com.welab.wefe.manager.service.api.union |
| Dependencies | ['com.welab.wefe.common.data.mongodb.repo.UnionNodeMongoRepo', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.web.api.base.AbstractApi', 'com.welab.wefe.common.web.api.base.Api', 'com.welab.wefe.common.web.dto.ApiResult', 'com.welab.wefe.manager.service.dto.base.BaseQueryInput', 'com.welab.wefe.manager.service.dto.union.UnionNodeQueryOutput', 'com.welab.wefe.manager.service.mapper.UnionNodeMapper', 'org.mapstruct.factory.Mappers', 'org.springframework.beans.factory.annotation.Autowired', 'java.util.List', 'java.util.stream.Collectors'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| QueryAllApi | class |  |



## Class QueryAllApi

|      |      |
|------|------|
| Access Modifier | @Api(path = "union/node/query", name = "union_node_query");public |
| Type | class |
| Name | QueryAllApi |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| unionNodeMongoRepo | UnionNodeMongoRepo |  |
| unionNodeMapper = Mappers.getMapper(UnionNodeMapper.class) | UnionNodeMapper |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| handle | ApiResult<JObject> |  |




