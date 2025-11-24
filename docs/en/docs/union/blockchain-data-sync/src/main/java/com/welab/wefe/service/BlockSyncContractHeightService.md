# Basic Information

|      |      |
|------|------|
| Name | BlockSyncContractHeightService |
| Language | .java |
| Code Path | WeFe/union/blockchain-data-sync/src/main/java/com/welab/wefe/service/BlockSyncContractHeightService.java |
| Package Name | com.welab.wefe.service |
| Dependencies | ['com.welab.wefe.bo.data.BlockInfoBO', 'com.welab.wefe.bo.data.EventBO', 'com.welab.wefe.common.data.mongodb.entity.union.BlockSyncContractHeight', 'com.welab.wefe.common.data.mongodb.repo.BlockSyncContractHeightMongoRepo', 'org.apache.commons.collections4.CollectionUtils', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.stereotype.Service', 'java.util.HashSet', 'java.util.List', 'java.util.Set'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| BlockSyncContractHeightService | class |  |



## Class BlockSyncContractHeightService

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | BlockSyncContractHeightService |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| blockSyncContractHeightMongoRepo | BlockSyncContractHeightMongoRepo |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| save | void |  |
| findByGroupIdAndContractName | BlockSyncContractHeight |  |
| upsertByGroupIdAndContractName | void |  |




