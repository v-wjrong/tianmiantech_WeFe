# Basic Information

|      |      |
|------|------|
| Name | DataSetTagsApi |
| Language | .java |
| Code Path | WeFe/manager/manager-service/src/main/java/com/welab/wefe/manager/service/api/dataset/DataSetTagsApi.java |
| Package Name | com.welab.wefe.manager.service.api.dataset |
| Dependencies | ['com.welab.wefe.common.data.mongodb.dto.dataset.DataSetTagsQueryOutput', 'com.welab.wefe.common.data.mongodb.repo.DataSetMongoReop', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.web.api.base.AbstractApi', 'com.welab.wefe.common.web.api.base.Api', 'com.welab.wefe.common.web.dto.ApiResult', 'com.welab.wefe.manager.service.dto.tag.ApiDataSetTagsQueryOutput', 'com.welab.wefe.manager.service.dto.tag.DataSetTagsQueryInput', 'com.welab.wefe.manager.service.dto.tag.TagsDTO', 'com.welab.wefe.manager.service.service.DataSetContractService', 'org.springframework.beans.factory.annotation.Autowired', 'java.util', 'java.util.stream.Collectors'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| DataSetTagsApi | class |  |



## Class DataSetTagsApi

|      |      |
|------|------|
| Access Modifier | @Api(path = "data_set/tags/query", name = "dataset_tags_query");public |
| Type | class |
| Name | DataSetTagsApi |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| dataSetMongoReop | DataSetMongoReop |  |
| mDatasetContractService | DataSetContractService |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| handle | ApiResult<ApiDataSetTagsQueryOutput> |  |
| convertTagList | List<TagsDTO> |  |




