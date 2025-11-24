# Basic Information

|      |      |
|------|------|
| Name | TaskService |
| Language | .java |
| Code Path | WeFe/fusion/fusion-service/src/main/java/com/welab/wefe/data/fusion/service/service/TaskService.java |
| Package Name | com.welab.wefe.data.fusion.service.service |
| Dependencies | ['com.alibaba.fastjson.JSONObject', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.data.mysql.Where', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.web.util.ModelMapper', 'com.welab.wefe.data.fusion.service.actuator.rsapsi.PsiServerActuator', 'com.welab.wefe.data.fusion.service.api.task', 'com.welab.wefe.data.fusion.service.database.entity.BloomFilterMySqlModel', 'com.welab.wefe.data.fusion.service.database.entity.DataSetMySqlModel', 'com.welab.wefe.data.fusion.service.database.entity.PartnerMySqlModel', 'com.welab.wefe.data.fusion.service.database.entity.TaskMySqlModel', 'com.welab.wefe.data.fusion.service.database.repository.DataSetRepository', 'com.welab.wefe.data.fusion.service.database.repository.PartnerRepository', 'com.welab.wefe.data.fusion.service.database.repository.TaskRepository', 'com.welab.wefe.data.fusion.service.dto.base.PagingOutput', 'com.welab.wefe.data.fusion.service.dto.entity.PartnerOutputModel', 'com.welab.wefe.data.fusion.service.dto.entity.TaskOutput', 'com.welab.wefe.data.fusion.service.dto.entity.TaskOverviewOutput', 'com.welab.wefe.data.fusion.service.dto.entity.bloomfilter.BloomfilterOutputModel', 'com.welab.wefe.data.fusion.service.dto.entity.dataset.DataSetOutputModel', 'com.welab.wefe.data.fusion.service.enums', 'com.welab.wefe.data.fusion.service.manager.ActuatorManager', 'com.welab.wefe.data.fusion.service.service.bloomfilter.BloomFilterService', 'com.welab.wefe.data.fusion.service.task.AbstractTask', 'com.welab.wefe.data.fusion.service.task.PsiServerTask', 'com.welab.wefe.data.fusion.service.utils.primarykey.FieldInfo', 'com.welab.wefe.data.fusion.service.utils.primarykey.PrimaryKeyUtils', 'org.apache.commons.collections4.CollectionUtils', 'org.apache.commons.lang3.StringUtils', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.data.jpa.domain.Specification', 'org.springframework.stereotype.Service', 'org.springframework.transaction.annotation.Transactional', 'java.math.BigInteger', 'java.util.Arrays', 'java.util.Date', 'java.util.List', 'java.util.UUID', 'java.util.concurrent', 'java.util.stream.Collectors', 'com.welab.wefe.common.StatusCode.DATA_NOT_FOUND', 'com.welab.wefe.common.StatusCode.PARAMETER_VALUE_INVALID'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| TaskService | class |  |



## Class TaskService

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | TaskService |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| partnerRepository | PartnerRepository |  |
| bloomFilterService | BloomFilterService |  |
| fieldInfoService | FieldInfoService |  |
| taskRepository | TaskRepository |  |
| partnerService | PartnerService |  |
| thirdPartyService | ThirdPartyService |  |
| taskResultService | TaskResultService |  |
| dataSetRepository | DataSetRepository |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| updateByBusinessId | void |  |
| paging | PagingOutput<TaskOutput> |  |
| findByBusinessId | TaskMySqlModel |  |
| psi | void |  |
| alignByPartner | void |  |
| psiClient | void |  |
| handle | void |  |
| update | void |  |
| find | TaskMySqlModel |  |
| psiServer | void |  |
| add | void |  |
| setDataResouceList | void |  |
| setPartnerList | void |  |
| delete | void |  |
| overview | TaskOverviewOutput |  |
| setName | void |  |
| detail | TaskOutput |  |




