# Basic Information

|      |      |
|------|------|
| Name | MemberServiceService |
| Language | .java |
| Code Path | WeFe/union/union-service/src/main/java/com/welab/wefe/union/service/service/MemberServiceService.java |
| Package Name | com.welab.wefe.union.service.service |
| Dependencies | ['com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.data.mongodb.dto.PageOutput', 'com.welab.wefe.common.data.mongodb.dto.member.MemberServiceQueryOutput', 'com.welab.wefe.common.data.mongodb.entity.union.MemberService', 'com.welab.wefe.common.data.mongodb.repo.MemberServiceMongoReop', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.union.service.api.service.PutApi', 'com.welab.wefe.union.service.api.service.QueryApi', 'com.welab.wefe.union.service.dto.member.ApiMemberServiceQueryOutput', 'com.welab.wefe.union.service.service.contract.MemberServiceContractService', 'com.welab.wefe.union.service.util.MapperUtil', 'com.welab.wefe.union.service.util.ModelMapper', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.stereotype.Service', 'java.util.List', 'java.util.stream.Collectors'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| MemberServiceService | class |  |



## Class MemberServiceService

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | MemberServiceService |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| memberServiceMongoReop | MemberServiceMongoReop |  |
| memberServiceContractService | MemberServiceContractService |  |
| LOG = LoggerFactory.getLogger(MemberServiceService.class) | Logger |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| query | PageOutput<ApiMemberServiceQueryOutput> |  |
| add | void |  |




