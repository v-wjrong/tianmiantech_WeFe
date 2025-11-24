# Basic Information

|      |      |
|------|------|
| Name | ContractContextInfo |
| Language | .java |
| Code Path | WeFe/union/blockchain-data-sync/src/main/java/com/welab/wefe/bo/contract/ContractContextInfo.java |
| Package Name | com.welab.wefe.bo.contract |
| Dependencies | ['com.welab.wefe.constant.BinConstant', 'com.welab.wefe.constant.SyncConstant', 'org.apache.commons.lang3.StringUtils', 'org.fisco.bcos.sdk.contract.precompiled.cns.CnsInfo', 'org.fisco.bcos.sdk.transaction.model.exception.ContractException', 'java.util.HashMap', 'java.util.List', 'java.util.Map', 'java.util.stream.Collectors'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| ContractContextInfo | class |  |



## Class ContractContextInfo

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | ContractContextInfo |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| CONTRACT_BINARY_MAP = new HashMap<>(16) | Map<String, ContractInfo> |  |
| CONTRACT_INFO_MAP = new HashMap<>(16) | Map<String, ContractInfo> |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getContractInfoByCode | ContractInfo |  |
| getContractInfoByContractName | ContractInfo |  |




