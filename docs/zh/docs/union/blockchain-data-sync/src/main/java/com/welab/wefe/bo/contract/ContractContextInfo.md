# 基础信息

|      |      |
|------|------|
| 名称 | ContractContextInfo |
| 编码语言 | .java |
| 代码路径 | WeFe/union/blockchain-data-sync/src/main/java/com/welab/wefe/bo/contract/ContractContextInfo.java |
| 包名 | com.welab.wefe.bo.contract |
| 依赖项 | ['com.welab.wefe.constant.BinConstant', 'com.welab.wefe.constant.SyncConstant', 'org.apache.commons.lang3.StringUtils', 'org.fisco.bcos.sdk.contract.precompiled.cns.CnsInfo', 'org.fisco.bcos.sdk.transaction.model.exception.ContractException', 'java.util.HashMap', 'java.util.List', 'java.util.Map', 'java.util.stream.Collectors'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| ContractContextInfo | class |  |



## 类 ContractContextInfo

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | ContractContextInfo |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| CONTRACT_BINARY_MAP = new HashMap<>(16) | Map<String, ContractInfo> |  |
| CONTRACT_INFO_MAP = new HashMap<>(16) | Map<String, ContractInfo> |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getContractInfoByCode | ContractInfo |  |
| getContractInfoByContractName | ContractInfo |  |




