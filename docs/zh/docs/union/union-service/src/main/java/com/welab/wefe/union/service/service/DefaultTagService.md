# 基础信息

|      |      |
|------|------|
| 名称 | DefaultTagService |
| 编码语言 | .java |
| 代码路径 | WeFe/union/union-service/src/main/java/com/welab/wefe/union/service/service/DefaultTagService.java |
| 包名 | com.welab.wefe.union.service.service |
| 依赖项 | ['com.welab.wefe.common.data.mongodb.entity.union.DataResourceDefaultTag', 'com.welab.wefe.common.data.mongodb.entity.union.DataSetDefaultTag', 'com.welab.wefe.common.data.mongodb.repo.DataResourceDefaultTagMongoRepo', 'com.welab.wefe.common.data.mongodb.repo.DataSetDefaultTagMongoRepo', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.wefe.enums.DataResourceType', 'com.welab.wefe.union.service.api.dataresource.DefaultTagQueryApi', 'com.welab.wefe.union.service.dto.base.BaseInput', 'com.welab.wefe.union.service.dto.dataresource.dataset.table.ApiDataSetDefaultTagOutput', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.stereotype.Service', 'java.util.List', 'java.util.stream.Collectors'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| DefaultTagService | class |  |



## 类 DefaultTagService

|      |      |
|------|------|
| 访问范围 | @Service;public |
| 类型 | class |
| 名称 | DefaultTagService |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| dataSetDefaultTagMongoRepo | DataSetDefaultTagMongoRepo |  |
| dataResourceDefaultTagMongoRepo | DataResourceDefaultTagMongoRepo |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| convertDataResourceType | String |  |
| query | List<ApiDataSetDefaultTagOutput> |  |
| queryAll | List<ApiDataSetDefaultTagOutput> |  |




