# Basic Information

|      |      |
|------|------|
| Name | AbstractDataResourceUpdateInputModel |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/dto/vo/data_resource/AbstractDataResourceUpdateInputModel.java |
| Package Name | com.welab.wefe.board.service.dto.vo.data_resource |
| Dependencies | ['com.welab.wefe.board.service.database.repository.data_resource.DataResourceRepository', 'com.welab.wefe.board.service.service.globalconfig.GlobalConfigService', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.fieldvalidate.annotation.Check', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.web.Launcher', 'com.welab.wefe.common.web.dto.AbstractApiInput', 'com.welab.wefe.common.wefe.dto.global_config.MemberInfoModel', 'com.welab.wefe.common.wefe.enums.DataResourcePublicLevel', 'org.apache.commons.lang3.StringUtils', 'java.util.List'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| AbstractDataResourceUpdateInputModel | class |  |



## Class AbstractDataResourceUpdateInputModel

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | AbstractDataResourceUpdateInputModel |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| name | String |  |
| description | String |  |
| publicMemberList | String |  |
| id | String |  |
| publicLevel | DataResourcePublicLevel |  |
| tags | List<String> |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getName | String |  |
| getDescription | String |  |
| setTags | void |  |
| setName | void |  |
| getId | String |  |
| setId | void |  |
| getTags | List<String> |  |
| checkAndStandardize | void |  |
| setDescription | void |  |
| getPublicLevel | DataResourcePublicLevel |  |
| setPublicLevel | void |  |
| getPublicMemberList | String |  |
| setPublicMemberList | void |  |




