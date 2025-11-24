# Basic Information

|      |      |
|------|------|
| Name | UpdateCertStatusApi |
| Language | .java |
| Code Path | WeFe/manager/manager-service/src/main/java/com/welab/wefe/manager/service/api/cert/UpdateCertStatusApi.java |
| Package Name | com.welab.wefe.manager.service.api.cert |
| Dependencies | ['com.webank.cert.mgr.model.vo.CertVO', 'com.webank.cert.mgr.service.CertOperationService', 'com.webank.cert.toolkit.enums.CertStatusEnums', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.data.mongodb.entity.union.Member', 'com.welab.wefe.common.data.mongodb.entity.union.ext.MemberExtJSON', 'com.welab.wefe.common.data.mongodb.repo.MemberMongoReop', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.fieldvalidate.annotation.Check', 'com.welab.wefe.common.web.api.base.AbstractApi', 'com.welab.wefe.common.web.api.base.Api', 'com.welab.wefe.common.web.dto.AbstractApiInput', 'com.welab.wefe.common.web.dto.ApiResult', 'com.welab.wefe.manager.service.api.cert.UpdateCertStatusApi.CertDetailInput', 'com.welab.wefe.manager.service.service.MemberContractService', 'org.springframework.beans.factory.annotation.Autowired'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| UpdateCertStatusApi | class |  |



## Class UpdateCertStatusApi

|      |      |
|------|------|
| Access Modifier | @Api(path = "cert/update_status", name = "update cert status");public |
| Type | class |
| Name | UpdateCertStatusApi |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| certOperationService | CertOperationService |  |
| memberContractService | MemberContractService |  |
| memberMongoReop | MemberMongoReop |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| handle | ApiResult<CertVO> |  |




