# Basic Information

|      |      |
|------|------|
| Name | TrustCertsContractService |
| Language | .java |
| Code Path | WeFe/manager/manager-service/src/main/java/com/welab/wefe/manager/service/service/TrustCertsContractService.java |
| Package Name | com.welab.wefe.manager.service.service |
| Dependencies | ['com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.data.mongodb.entity.union.TrustCerts', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.manager.service.contract.TrustCertsContract', 'org.fisco.bcos.sdk.crypto.CryptoSuite', 'org.fisco.bcos.sdk.model.TransactionReceipt', 'org.fisco.bcos.sdk.transaction.codec.decode.TransactionDecoderService', 'org.fisco.bcos.sdk.transaction.model.dto.TransactionResponse', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.stereotype.Service', 'java.util.ArrayList', 'java.util.List'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| TrustCertsContractService | class |  |



## Class TrustCertsContractService

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | TrustCertsContractService |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| trustCertsContract | TrustCertsContract |  |
| cryptoSuite | CryptoSuite |  |
| LOG = LoggerFactory.getLogger(TrustCertsContractService.class) | Logger |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| deleteBySerialNumber | void |  |
| add | void |  |
| isExistBySerialNumber | boolean |  |
| generateAddParams | List<String> |  |




