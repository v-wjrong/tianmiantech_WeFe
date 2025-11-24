# Basic Information

|      |      |
|------|------|
| Name | DataSyncTask |
| Language | .java |
| Code Path | WeFe/union/blockchain-data-sync/src/main/java/com/welab/wefe/task/DataSyncTask.java |
| Package Name | com.welab.wefe.task |
| Dependencies | ['com.welab.wefe.bo.data.BlockInfoBO', 'com.welab.wefe.bo.data.EventBO', 'com.welab.wefe.common.data.mongodb.entity.union.BlockSyncContractHeight', 'com.welab.wefe.common.data.mongodb.entity.union.BlockSyncHeight', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.util.ThreadUtil', 'com.welab.wefe.constant.BlockConstant', 'com.welab.wefe.constant.SyncConstant', 'com.welab.wefe.exception.BusinessException', 'com.welab.wefe.parser.BlockInfoParser', 'com.welab.wefe.service.BlockSyncContractHeightService', 'com.welab.wefe.service.BlockSyncDetailInfoService', 'com.welab.wefe.service.BlockSyncHeightService', 'com.welab.wefe.service.TransactionResponseService', 'com.welab.wefe.tool.DataProcessor', 'com.welab.wefe.tool.DataSyncContext', 'com.welab.wefe.util.BlockUtil', 'org.apache.commons.collections4.CollectionUtils', 'org.apache.commons.lang.math.NumberUtils', 'org.fisco.bcos.sdk.BcosSDK', 'org.fisco.bcos.sdk.client.Client', 'org.fisco.bcos.sdk.client.protocol.response.BcosBlock', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.beans.BeanUtils', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.beans.factory.annotation.Value', 'org.springframework.stereotype.Component', 'java.math.BigInteger', 'java.util.ArrayList', 'java.util.List'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| DataSyncTask | class |  |



## Class DataSyncTask

|      |      |
|------|------|
| Access Modifier | @Component;public |
| Type | class |
| Name | DataSyncTask |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| LOG = LoggerFactory.getLogger(DataSyncTask.class) | Logger |  |
| wechatUrl | String |  |
| blockSyncDetailInfoService | BlockSyncDetailInfoService |  |
| bcosSDK | BcosSDK |  |
| blockSyncHeightService | BlockSyncHeightService |  |
| blockSyncContractHeightService | BlockSyncContractHeightService |  |
| dataSyncGroupId | String |  |
| transactionResponseService | TransactionResponseService |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| startTask | void |  |




