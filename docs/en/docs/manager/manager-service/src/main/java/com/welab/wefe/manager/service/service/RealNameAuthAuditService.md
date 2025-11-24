# Basic Information

|      |      |
|------|------|
| Name | RealNameAuthAuditService |
| Language | .java |
| Code Path | WeFe/manager/manager-service/src/main/java/com/welab/wefe/manager/service/service/RealNameAuthAuditService.java |
| Package Name | com.welab.wefe.manager.service.service |
| Dependencies | ['com.webank.cert.mgr.model.vo.CertVO', 'com.webank.cert.mgr.service.CertOperationService', 'com.webank.cert.toolkit.enums.CertStatusEnums', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.data.mongodb.dto.PageOutput', 'com.welab.wefe.common.data.mongodb.entity.manager.CertInfo', 'com.welab.wefe.common.data.mongodb.entity.union.Member', 'com.welab.wefe.common.data.mongodb.entity.union.ext.MemberExtJSON', 'com.welab.wefe.common.data.mongodb.repo.MemberMongoReop', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.manager.service.dto.member.RealNameAuthInput', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.stereotype.Service', 'org.springframework.util.CollectionUtils', 'javax.transaction.Transactional', 'java.util.List'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| RealNameAuthAuditService | class |  |



## Class RealNameAuthAuditService

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | RealNameAuthAuditService |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| certOperationService | CertOperationService |  |
| memberMongoReop | MemberMongoReop |  |
| memberContractService | MemberContractService |  |
| LOG = LoggerFactory.getLogger(RealNameAuthAuditService.class) | Logger |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| audit | void |  |




