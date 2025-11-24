# Basic Information

|      |      |
|------|------|
| Name | DefaultTagService |
| Language | .java |
| Code Path | WeFe/union/union-service/src/main/java/com/welab/wefe/union/service/service/DefaultTagService.java |
| Package Name | com.welab.wefe.union.service.service |
| Dependencies | ['com.welab.wefe.common.data.mongodb.entity.union.DataResourceDefaultTag', 'com.welab.wefe.common.data.mongodb.entity.union.DataSetDefaultTag', 'com.welab.wefe.common.data.mongodb.repo.DataResourceDefaultTagMongoRepo', 'com.welab.wefe.common.data.mongodb.repo.DataSetDefaultTagMongoRepo', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.wefe.enums.DataResourceType', 'com.welab.wefe.union.service.api.dataresource.DefaultTagQueryApi', 'com.welab.wefe.union.service.dto.base.BaseInput', 'com.welab.wefe.union.service.dto.dataresource.dataset.table.ApiDataSetDefaultTagOutput', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.stereotype.Service', 'java.util.List', 'java.util.stream.Collectors'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| DefaultTagService | class |  |



## Class DefaultTagService

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | DefaultTagService |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| dataSetDefaultTagMongoRepo | DataSetDefaultTagMongoRepo |  |
| dataResourceDefaultTagMongoRepo | DataResourceDefaultTagMongoRepo |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| convertDataResourceType | String |  |
| query | List<ApiDataSetDefaultTagOutput> |  |
| queryAll | List<ApiDataSetDefaultTagOutput> |  |




