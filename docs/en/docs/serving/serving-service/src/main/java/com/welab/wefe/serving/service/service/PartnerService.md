# Basic Information

|      |      |
|------|------|
| Name | PartnerService |
| Language | .java |
| Code Path | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/service/PartnerService.java |
| Package Name | com.welab.wefe.serving.service.service |
| Dependencies | ['java.util.Date', 'java.util.List', 'java.util.UUID', 'java.util.stream.Collectors', 'org.apache.commons.collections.CollectionUtils', 'org.apache.commons.lang3.StringUtils', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.data.jpa.domain.Specification', 'org.springframework.stereotype.Service', 'org.springframework.transaction.annotation.Transactional', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.data.mysql.Where', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.web.util.CurrentAccountUtil', 'com.welab.wefe.common.web.util.ModelMapper', 'com.welab.wefe.serving.service.api.member.QueryApi', 'com.welab.wefe.serving.service.api.partner.DetailPartnerApi', 'com.welab.wefe.serving.service.api.partner.QueryPartnerAllApi', 'com.welab.wefe.serving.service.api.partner.QueryPartnerListApi', 'com.welab.wefe.serving.service.api.partner.QueryPartnerListApi.Input', 'com.welab.wefe.serving.service.api.partner.QueryPartnerListApi.Output', 'com.welab.wefe.serving.service.api.partner.SavePartnerApi', 'com.welab.wefe.serving.service.database.entity.ClientMysqlModel', 'com.welab.wefe.serving.service.database.entity.ClientServiceMysqlModel', 'com.welab.wefe.serving.service.database.entity.MemberMySqlModel', 'com.welab.wefe.serving.service.database.entity.PartnerMysqlModel', 'com.welab.wefe.serving.service.database.repository.ClientRepository', 'com.welab.wefe.serving.service.database.repository.ClientServiceRepository', 'com.welab.wefe.serving.service.database.repository.MemberRepository', 'com.welab.wefe.serving.service.database.repository.PartnerRepository', 'com.welab.wefe.serving.service.dto.MemberParams', 'com.welab.wefe.serving.service.dto.PagingOutput', 'com.welab.wefe.serving.service.enums.ClientStatusEnum'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| PartnerService | class |  |



## Class PartnerService

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | PartnerService |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| clientServiceRepository | ClientServiceRepository |  |
| clientRepository | ClientRepository |  |
| memberRepository | MemberRepository |  |
| partnerRepository | PartnerRepository |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| upsert | void |  |
| update | void |  |
| queryByName | DetailPartnerApi.Output |  |
| upsert | void |  |
| queryList | PagingOutput<Output> |  |
| queryByCode | PartnerMysqlModel |  |
| queryById | DetailPartnerApi.Output |  |
| init | void |  |
| query | PagingOutput<QueryApi.Output> |  |
| queryByClientName | ClientMysqlModel |  |
| delete | void |  |
| queryAll | List<QueryPartnerAllApi.Output> |  |
| save | void |  |
| findOne | PartnerMysqlModel |  |
| findModelServiceUrl | String |  |
| queryByPartnerName | PartnerMysqlModel |  |




