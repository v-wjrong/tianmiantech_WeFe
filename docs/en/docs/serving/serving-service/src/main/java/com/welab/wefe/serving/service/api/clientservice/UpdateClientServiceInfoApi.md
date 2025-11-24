# Basic Information

|      |      |
|------|------|
| Name | UpdateClientServiceInfoApi |
| Language | .java |
| Code Path | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/api/clientservice/UpdateClientServiceInfoApi.java |
| Package Name | com.welab.wefe.serving.service.api.clientservice |
| Dependencies | ['com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.web.api.base.AbstractNoneInputApi', 'com.welab.wefe.common.web.api.base.Api', 'com.welab.wefe.common.web.dto.AbstractApiOutput', 'com.welab.wefe.common.web.dto.ApiResult', 'com.welab.wefe.serving.service.database.entity.ClientMysqlModel', 'com.welab.wefe.serving.service.database.entity.ClientServiceMysqlModel', 'com.welab.wefe.serving.service.database.repository.ClientServiceRepository', 'com.welab.wefe.serving.service.enums.ServiceClientTypeEnum', 'com.welab.wefe.serving.service.service.ClientService', 'com.welab.wefe.serving.service.service.ClientServiceService', 'org.springframework.beans.factory.annotation.Autowired', 'java.util.List'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| UpdateClientServiceInfoApi | class |  |



## Class UpdateClientServiceInfoApi

|      |      |
|------|------|
| Access Modifier | @Api(path = "clientservice/update_client_service_info", name = "update client service info");public |
| Type | class |
| Name | UpdateClientServiceInfoApi |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| clientService | ClientService |  |
| clientServiceService | ClientServiceService |  |
| clientServiceRepository | ClientServiceRepository |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| handle | ApiResult<Output> |  |




