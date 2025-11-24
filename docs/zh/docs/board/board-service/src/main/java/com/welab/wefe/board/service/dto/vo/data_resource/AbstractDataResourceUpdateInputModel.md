# 基础信息

|      |      |
|------|------|
| 名称 | AbstractDataResourceUpdateInputModel |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/dto/vo/data_resource/AbstractDataResourceUpdateInputModel.java |
| 包名 | com.welab.wefe.board.service.dto.vo.data_resource |
| 依赖项 | ['com.welab.wefe.board.service.database.repository.data_resource.DataResourceRepository', 'com.welab.wefe.board.service.service.globalconfig.GlobalConfigService', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.fieldvalidate.annotation.Check', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.web.Launcher', 'com.welab.wefe.common.web.dto.AbstractApiInput', 'com.welab.wefe.common.wefe.dto.global_config.MemberInfoModel', 'com.welab.wefe.common.wefe.enums.DataResourcePublicLevel', 'org.apache.commons.lang3.StringUtils', 'java.util.List'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| AbstractDataResourceUpdateInputModel | class |  |



## 类 AbstractDataResourceUpdateInputModel

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | AbstractDataResourceUpdateInputModel |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| name | String |  |
| description | String |  |
| publicMemberList | String |  |
| id | String |  |
| publicLevel | DataResourcePublicLevel |  |
| tags | List<String> |  |

### 方法列表

| 名称  | 类型  | 说明 |
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




