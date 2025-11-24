# Basic Information

|      |      |
|------|------|
| Name | ModelMemberService |
| Language | .java |
| Code Path | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/service/ModelMemberService.java |
| Package Name | com.welab.wefe.serving.service.service |
| Dependencies | ['com.google.common.collect.Lists', 'com.welab.wefe.common.data.mysql.Where', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.web.util.ModelMapper', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'com.welab.wefe.serving.sdk.dto.ProviderParams', 'com.welab.wefe.serving.service.database.entity.ModelMemberBaseModel', 'com.welab.wefe.serving.service.database.entity.ModelMemberMySqlModel', 'com.welab.wefe.serving.service.database.entity.PartnerMysqlModel', 'com.welab.wefe.serving.service.database.repository.ModelMemberBaseRepository', 'com.welab.wefe.serving.service.database.repository.ModelMemberRepository', 'com.welab.wefe.serving.service.dto.MemberParams', 'com.welab.wefe.serving.service.dto.ModelStatusOutput', 'com.welab.wefe.serving.service.enums.MemberModelStatusEnum', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.data.jpa.domain.Specification', 'org.springframework.stereotype.Service', 'java.util.Date', 'java.util.List', 'java.util.TreeMap', 'java.util.stream.Collectors'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| ModelMemberService | class |  |



## Class ModelMemberService

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | ModelMemberService |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| serviceService | ServiceService |  |
| modelMemberBaseRepository | ModelMemberBaseRepository |  |
| LOG = LoggerFactory.getLogger(getClass()) | Logger |  |
| modelMemberRepository | ModelMemberRepository |  |
| partnerService | PartnerService |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| findListByModelIdAndMemberId | List<ModelMemberMySqlModel> |  |
| isProvider | boolean |  |
| checkAvailableByModelIdAndMemberId | List<ModelStatusOutput> |  |
| checkAvailable | ModelStatusOutput |  |
| save | void |  |
| save | void |  |
| findProviders | List<ProviderParams> |  |
| findPartnerUrl | String |  |
| updateModelStatus | void |  |
| findModelMemberBase | List<ModelMemberBaseModel> |  |
| callProvider | ModelStatusOutput |  |
| findServingBaseUrl | String |  |




