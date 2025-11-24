# Basic Information

|      |      |
|------|------|
| Name | ModelService |
| Language | .java |
| Code Path | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/service/ModelService.java |
| Package Name | com.welab.wefe.serving.service.service |
| Dependencies | ['com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.data.mysql.Where', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.web.util.CurrentAccountUtil', 'com.welab.wefe.common.web.util.ModelMapper', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'com.welab.wefe.common.wefe.enums.PredictFeatureDataSource', 'com.welab.wefe.serving.service.api.model.EnableApi', 'com.welab.wefe.serving.service.api.model.QueryApi', 'com.welab.wefe.serving.service.api.model.SaveModelApi', 'com.welab.wefe.serving.service.database.entity.ModelMemberMySqlModel', 'com.welab.wefe.serving.service.database.entity.TableModelMySqlModel', 'com.welab.wefe.serving.service.database.repository.ModelMemberRepository', 'com.welab.wefe.serving.service.database.repository.TableModelRepository', 'com.welab.wefe.serving.service.dto.MemberParams', 'com.welab.wefe.serving.service.dto.ModelStatusOutput', 'com.welab.wefe.serving.service.dto.PagingOutput', 'com.welab.wefe.serving.service.enums.MemberModelStatusEnum', 'com.welab.wefe.serving.service.enums.ServiceTypeEnum', 'com.welab.wefe.serving.service.manager.ModelManager', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.beans.BeanUtils', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.data.jpa.domain.Specification', 'org.springframework.stereotype.Service', 'org.springframework.transaction.annotation.Transactional', 'java.util.Date', 'java.util.List', 'java.util.stream.Collectors'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| ModelService | class |  |



## Class ModelService

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | ModelService |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| partnerService | PartnerService |  |
| API_PREFIX_1 = "/api/" | String |  |
| clientServiceService | ClientServiceService |  |
| modelRepository | TableModelRepository |  |
| LOG = LoggerFactory.getLogger(getClass()) | Logger |  |
| modelMemberRepository | ModelMemberRepository |  |
| API_PREFIX_2 = "predict/" | String |  |
| modelMemberService | ModelMemberService |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| findOne | TableModelMySqlModel |  |
| activate | void |  |
| convertTo | TableModelMySqlModel |  |
| findByModelIdAndMemberId | List<ModelMemberMySqlModel> |  |
| bulidOutputs | List<QueryApi.Output> |  |
| save | String |  |
| queryModelMembers | PagingOutput<ModelMemberMySqlModel> |  |
| query | PagingOutput<QueryApi.Output> |  |
| setModelServiceUrl | String |  |
| upsertModel | String |  |
| saveModelMembers | void |  |
| buildQueryMemberParam | Specification<ModelMemberMySqlModel> |  |
| openPartnerService | void |  |
| findByModelIdAndMemberIdAndRole | ModelMemberMySqlModel |  |
| openService | void |  |
| activatePartnerService | void |  |
| queryModels | PagingOutput<TableModelMySqlModel> |  |
| buildQueryModelParam | Specification<TableModelMySqlModel> |  |
| enable | void |  |
| getAvailableStatus | MemberModelStatusEnum |  |
| updateConfig | void |  |
| checkAvailable | ModelStatusOutput |  |
| openService | void |  |
| setRole | QueryApi.Output |  |
| addPartners | void |  |




