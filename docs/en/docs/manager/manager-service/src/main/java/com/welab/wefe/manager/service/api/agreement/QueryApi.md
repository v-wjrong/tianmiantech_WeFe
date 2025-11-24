# Basic Information

|      |      |
|------|------|
| Name | QueryApi |
| Language | .java |
| Code Path | WeFe/manager/manager-service/src/main/java/com/welab/wefe/manager/service/api/agreement/QueryApi.java |
| Package Name | com.welab.wefe.manager.service.api.agreement |
| Dependencies | ['com.welab.wefe.common.data.mongodb.repo.RealnameAuthAgreementTemplateMongoRepo', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.web.api.base.AbstractApi', 'com.welab.wefe.common.web.api.base.Api', 'com.welab.wefe.common.web.dto.ApiResult', 'com.welab.wefe.manager.service.dto.agreement.RealnameAuthAgreementTemplateOutput', 'com.welab.wefe.manager.service.dto.base.BaseInput', 'com.welab.wefe.manager.service.mapper.RealnameAuthAgreementTemplateMapper', 'org.mapstruct.factory.Mappers', 'org.springframework.beans.factory.annotation.Autowired', 'java.util.List', 'java.util.stream.Collectors'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| QueryApi | class |  |



## Class QueryApi

|      |      |
|------|------|
| Access Modifier | @Api(path = "realname/auth/agreement/template/query", name = "realname_auth_agreement_template_query");public |
| Type | class |
| Name | QueryApi |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| mapper = Mappers.getMapper(RealnameAuthAgreementTemplateMapper.class) | RealnameAuthAgreementTemplateMapper |  |
| realnameAuthAgreementTemplateMongoRepo | RealnameAuthAgreementTemplateMongoRepo |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| handle | ApiResult<JObject> |  |




