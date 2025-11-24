# 基础信息

|      |      |
|------|------|
| 名称 | DataResourceTagsApi |
| 编码语言 | .java |
| 代码路径 | WeFe/manager/manager-service/src/main/java/com/welab/wefe/manager/service/api/dataresource/DataResourceTagsApi.java |
| 包名 | com.welab.wefe.manager.service.api.dataresource |
| 依赖项 | ['com.welab.wefe.common.data.mongodb.repo.DataResourceMongoReop', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.web.api.base.AbstractApi', 'com.welab.wefe.common.web.api.base.Api', 'com.welab.wefe.common.web.dto.AbstractApiInput', 'com.welab.wefe.common.web.dto.ApiResult', 'com.welab.wefe.manager.service.dto.tag.TagsDTO', 'org.springframework.beans.factory.annotation.Autowired', 'java.io.IOException', 'java.util.Arrays', 'java.util.Comparator', 'java.util.List', 'java.util.Map', 'java.util.stream.Collectors'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| DataResourceTagsApi | class |  |



## 类 DataResourceTagsApi

|      |      |
|------|------|
| 访问范围 | @Api(path = "data_resource/tags/query", name = "data_resource_tags_query");public |
| 类型 | class |
| 名称 | DataResourceTagsApi |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| dataResourceMongoReop | DataResourceMongoReop |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| handle | ApiResult<List<TagsDTO>> |  |




