# Basic Information

|      |      |
|------|------|
| Name | ClientService |
| Language | .java |
| Code Path | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/service/ClientService.java |
| Package Name | com.welab.wefe.serving.service.service |
| Dependencies | ['com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.data.mysql.Where', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.web.util.ModelMapper', 'com.welab.wefe.serving.service.api.client.QueryClientApi', 'com.welab.wefe.serving.service.api.client.QueryClientListApi', 'com.welab.wefe.serving.service.api.client.SaveClientApi', 'com.welab.wefe.serving.service.api.client.UpdateApi', 'com.welab.wefe.serving.service.database.entity.ClientMysqlModel', 'com.welab.wefe.serving.service.database.entity.ClientServiceMysqlModel', 'com.welab.wefe.serving.service.database.repository.ClientRepository', 'com.welab.wefe.serving.service.database.repository.ClientServiceRepository', 'com.welab.wefe.serving.service.dto.PagingOutput', 'com.welab.wefe.serving.service.enums.ClientStatusEnum', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.data.jpa.domain.Specification', 'org.springframework.stereotype.Service', 'java.util.Date', 'java.util.List', 'java.util.stream.Collectors'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| ClientService | class |  |



## Class ClientService

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | ClientService |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| clientRepository | ClientRepository |  |
| clientServiceRepository | ClientServiceRepository |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| queryByCode | ClientMysqlModel |  |
| queryByServiceIdAndClientId | ClientServiceMysqlModel |  |
| queryByClientName | ClientMysqlModel |  |
| update | void |  |
| queryList | PagingOutput<QueryClientListApi.Output> |  |
| save | void |  |
| detele | void |  |
| queryByClientId | ClientMysqlModel |  |
| queryById | QueryClientApi.Output |  |
| queryByName | QueryClientApi.Output |  |




