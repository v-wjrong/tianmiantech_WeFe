# Basic Information

|      |      |
|------|------|
| Name | MemberAuthTypeContractService |
| Language | .java |
| Code Path | WeFe/manager/manager-service/src/main/java/com/welab/wefe/manager/service/service/MemberAuthTypeContractService.java |
| Package Name | com.welab.wefe.manager.service.service |
| Dependencies | ['com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.data.mongodb.entity.union.MemberAuthType', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.DateUtil', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.manager.service.contract.MemberAuthTypeContract', 'com.welab.wefe.manager.service.dto.authtype.MemberAuthTypeUpdateInput', 'org.fisco.bcos.sdk.crypto.CryptoSuite', 'org.fisco.bcos.sdk.model.TransactionReceipt', 'org.fisco.bcos.sdk.transaction.codec.decode.TransactionDecoderService', 'org.fisco.bcos.sdk.transaction.model.dto.TransactionResponse', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.stereotype.Service', 'java.util.ArrayList', 'java.util.Date', 'java.util.List'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| MemberAuthTypeContractService | class |  |



## Class MemberAuthTypeContractService

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | MemberAuthTypeContractService |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| memberAuthTypeContract | MemberAuthTypeContract |  |
| LOG = LoggerFactory.getLogger(MemberAuthTypeContractService.class) | Logger |  |
| cryptoSuite | CryptoSuite |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| updateByTypeId | void |  |
| add | void |  |
| deleteByTypeId | void |  |
| generateParams | List<String> |  |




