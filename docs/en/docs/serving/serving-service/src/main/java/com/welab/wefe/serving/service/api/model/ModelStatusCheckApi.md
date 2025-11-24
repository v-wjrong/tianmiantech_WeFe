# Basic Information

|      |      |
|------|------|
| Name | ModelStatusCheckApi |
| Language | .java |
| Code Path | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/api/model/ModelStatusCheckApi.java |
| Package Name | com.welab.wefe.serving.service.api.model |
| Dependencies | ['com.welab.wefe.common.fieldvalidate.annotation.Check', 'com.welab.wefe.common.web.api.base.AbstractApi', 'com.welab.wefe.common.web.api.base.Api', 'com.welab.wefe.common.web.dto.AbstractApiInput', 'com.welab.wefe.common.web.dto.AbstractApiOutput', 'com.welab.wefe.common.web.dto.ApiResult', 'com.welab.wefe.serving.service.dto.ModelStatusOutput', 'com.welab.wefe.serving.service.enums.MemberModelStatusEnum', 'com.welab.wefe.serving.service.service.ModelMemberService', 'org.springframework.beans.factory.annotation.Autowired', 'java.util.List'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| ModelStatusCheckApi | class |  |



## Class ModelStatusCheckApi

|      |      |
|------|------|
| Access Modifier | @Api(path = "model/status/check", name = "检查模型状态");public |
| Type | class |
| Name | ModelStatusCheckApi |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| modelMemberService | ModelMemberService |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| handle | ApiResult<List<ModelStatusOutput>> |  |




