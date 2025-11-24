# Basic Information

|      |      |
|------|------|
| Name | DataSetMemberPermissionContractService |
| Language | .java |
| Code Path | WeFe/union/union-service/src/main/java/com/welab/wefe/union/service/service/contract/DataSetMemberPermissionContractService.java |
| Package Name | com.welab.wefe.union.service.service.contract |
| Dependencies | ['com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.DateUtil', 'com.welab.wefe.union.service.contract.DataSetMemberPermissionContract', 'com.welab.wefe.union.service.entity.DataSetMemberPermission', 'org.fisco.bcos.sdk.crypto.CryptoSuite', 'org.fisco.bcos.sdk.model.TransactionReceipt', 'org.fisco.bcos.sdk.transaction.codec.decode.TransactionDecoderService', 'org.fisco.bcos.sdk.transaction.model.dto.TransactionResponse', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.stereotype.Service', 'java.math.BigInteger', 'java.util.Arrays', 'java.util.List', 'java.util.stream.Collectors'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| DataSetMemberPermissionContractService | class |  |



## Class DataSetMemberPermissionContractService

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | DataSetMemberPermissionContractService |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| memberContractService | MemberContractService |  |
| dataSetMemberPermissionContract | DataSetMemberPermissionContract |  |
| LOG = LoggerFactory.getLogger(DataSetMemberPermissionContractService.class) | Logger |  |
| cryptoSuite | CryptoSuite |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| save | void |  |
| deleteByDataSetId | void |  |
| validateMembersLocal | void |  |
| validateMembersRemote | void |  |




