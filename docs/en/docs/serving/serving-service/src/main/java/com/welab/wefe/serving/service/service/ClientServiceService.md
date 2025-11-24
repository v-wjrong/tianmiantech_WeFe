# Basic Information

|      |      |
|------|------|
| Name | ClientServiceService |
| Language | .java |
| Code Path | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/service/ClientServiceService.java |
| Package Name | com.welab.wefe.serving.service.service |
| Dependencies | ['cn.hutool.core.lang.UUID', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.constant.SecretKeyType', 'com.welab.wefe.common.data.mysql.Where', 'com.welab.wefe.common.data.mysql.enums.OrderBy', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.http.HttpRequest', 'com.welab.wefe.common.http.HttpResponse', 'com.welab.wefe.common.util.SignUtil', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.web.util.CurrentAccountUtil', 'com.welab.wefe.common.web.util.ModelMapper', 'com.welab.wefe.serving.sdk.dto.ProviderParams', 'com.welab.wefe.serving.service.api.clientservice', 'com.welab.wefe.serving.service.api.clientservice.ServiceUrlTestApi.Input', 'com.welab.wefe.serving.service.database.entity', 'com.welab.wefe.serving.service.database.repository', 'com.welab.wefe.serving.service.dto.PagingOutput', 'com.welab.wefe.serving.service.enums.PayTypeEnum', 'com.welab.wefe.serving.service.enums.ServiceClientTypeEnum', 'com.welab.wefe.serving.service.enums.ServiceStatusEnum', 'com.welab.wefe.serving.service.enums.ServiceTypeEnum', 'com.welab.wefe.serving.service.utils.ServiceUtil', 'org.apache.commons.lang3.StringUtils', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.data.jpa.domain.Specification', 'org.springframework.stereotype.Service', 'java.util.ArrayList', 'java.util.Date', 'java.util.List', 'java.util.Optional', 'java.util.stream.Collectors'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| ClientServiceService | class |  |



## Class ClientServiceService

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | ClientServiceService |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| partnerService | PartnerService |  |
| clientServiceQueryRepository | ClientServiceQueryRepository |  |
| partnerRepository | PartnerRepository |  |
| clientServiceRepository | ClientServiceRepository |  |
| feeConfigRepository | FeeConfigRepository |  |
| serviceRepository | BaseServiceRepository<BaseServiceMySqlModel> |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| activateService | void |  |
| getAll | List<ClientServiceMysqlModel> |  |
| updateStatus | void |  |
| detail | ClientServiceOutputModel |  |
| deleteActivate | void |  |
| queryList | PagingOutput<QueryListApi.Output> |  |
| findActivateClientServiceByUrl | ClientServiceMysqlModel |  |
| update | void |  |
| add | void |  |
| openService | void |  |
| serviceUrlTest | int |  |
| updateAllByServiceId | void |  |
| queryByIdAndServiceId | ClientServiceMysqlModel |  |
| queryOne | ClientServiceOutputModel |  |
| queryByServiceIdAndClientId | ClientServiceMysqlModel |  |
| queryActivateListByServiceId | List<ClientServiceMysqlModel> |  |
| findProviderList | List<ProviderParams> |  |




