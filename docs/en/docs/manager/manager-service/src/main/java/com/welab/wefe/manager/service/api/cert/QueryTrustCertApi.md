# Basic Information

|      |      |
|------|------|
| Name | QueryTrustCertApi |
| Language | .java |
| Code Path | WeFe/manager/manager-service/src/main/java/com/welab/wefe/manager/service/api/cert/QueryTrustCertApi.java |
| Package Name | com.welab.wefe.manager.service.api.cert |
| Dependencies | ['com.welab.wefe.common.data.mongodb.repo.TrustCertsMongoRepo', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.web.api.base.AbstractApi', 'com.welab.wefe.common.web.api.base.Api', 'com.welab.wefe.common.web.dto.ApiResult', 'com.welab.wefe.manager.service.dto.base.BaseQueryInput', 'com.welab.wefe.manager.service.dto.cert.TrustCertsQueryOutput', 'com.welab.wefe.manager.service.mapper.TrustCertsMapper', 'org.mapstruct.factory.Mappers', 'org.springframework.beans.factory.annotation.Autowired', 'java.util.List', 'java.util.stream.Collectors'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| QueryTrustCertApi | class |  |



## Class QueryTrustCertApi

|      |      |
|------|------|
| Access Modifier | @Api(path = "trust/certs/query", name = "trust_cert_query");public |
| Type | class |
| Name | QueryTrustCertApi |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| mMapper = Mappers.getMapper(TrustCertsMapper.class) | TrustCertsMapper |  |
| trustCertsMongoRepo | TrustCertsMongoRepo |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| handle | ApiResult<JObject> |  |




