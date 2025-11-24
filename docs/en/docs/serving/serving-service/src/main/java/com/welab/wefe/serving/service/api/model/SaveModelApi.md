# Basic Information

|      |      |
|------|------|
| Name | SaveModelApi |
| Language | .java |
| Code Path | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/api/model/SaveModelApi.java |
| Package Name | com.welab.wefe.serving.service.api.model |
| Dependencies | ['java.util.List', 'java.util.Map', 'org.springframework.beans.factory.annotation.Autowired', 'com.welab.wefe.common.fieldvalidate.annotation.Check', 'com.welab.wefe.common.web.api.base.AbstractNoneOutputApi', 'com.welab.wefe.common.web.api.base.Api', 'com.welab.wefe.common.web.api.base.Caller', 'com.welab.wefe.common.web.dto.AbstractApiInput', 'com.welab.wefe.common.web.dto.ApiResult', 'com.welab.wefe.common.wefe.enums.Algorithm', 'com.welab.wefe.common.wefe.enums.FederatedLearningType', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'com.welab.wefe.serving.service.dto.MemberParams', 'com.welab.wefe.serving.service.service.ModelService'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| SaveModelApi | class |  |



## Class SaveModelApi

|      |      |
|------|------|
| Access Modifier | @Api(;        path = "model_save",;        name = "保存模型信息",;        allowAccessWithSign = true,;        domain = Caller.Board;);public |
| Type | class |
| Name | SaveModelApi |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| modelService | ModelService |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| handler | ApiResult<?> |  |




