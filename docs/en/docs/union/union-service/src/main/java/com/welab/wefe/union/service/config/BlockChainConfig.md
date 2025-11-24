# Basic Information

|      |      |
|------|------|
| Name | BlockChainConfig |
| Language | .java |
| Code Path | WeFe/union/union-service/src/main/java/com/welab/wefe/union/service/config/BlockChainConfig.java |
| Package Name | com.welab.wefe.union.service.config |
| Dependencies | ['com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.wefe.enums.ContractName', 'com.welab.wefe.union.service.contract', 'io.netty.channel.ChannelHandlerContext', 'org.apache.commons.collections4.CollectionUtils', 'org.fisco.bcos.sdk.BcosSDK', 'org.fisco.bcos.sdk.client.Client', 'org.fisco.bcos.sdk.config.ConfigOption', 'org.fisco.bcos.sdk.config.model.ConfigProperty', 'org.fisco.bcos.sdk.contract.precompiled.cns.CnsInfo', 'org.fisco.bcos.sdk.contract.precompiled.cns.CnsService', 'org.fisco.bcos.sdk.crypto.CryptoSuite', 'org.fisco.bcos.sdk.crypto.keypair.CryptoKeyPair', 'org.fisco.bcos.sdk.model.Message', 'org.fisco.bcos.sdk.model.NodeVersion.ClientVersion', 'org.fisco.bcos.sdk.network.MsgHandler', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.boot.context.properties.ConfigurationProperties', 'org.springframework.context.annotation.Bean', 'org.springframework.context.annotation.Configuration', 'java.util.ArrayList', 'java.util.HashMap', 'java.util.List', 'java.util.Map'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| BlockChainConfig | class |  |



## Class BlockChainConfig

|      |      |
|------|------|
| Access Modifier | @Configuration;@ConfigurationProperties(prefix = "block.chain");public |
| Type | class |
| Name | BlockChainConfig |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| log =            LoggerFactory.getLogger(BlockChainConfig.class) | Logger |  |
| corePoolSize | String |  |
| PEER_CONNECTED = true | boolean |  |
| channelPort = "20200" | String |  |
| maxPoolSize | String |  |
| certPath = "conf" | String |  |
| groupId | int |  |
| ip = "127.0.0.1" | String |  |
| queueCapacity | String |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getCertPath | String |  |
| getCurrentBlockchainNodeId | String |  |
| setQueueCapacity | void |  |
| getIp | String |  |
| setIp | void |  |
| getChannelPort | String |  |
| setChannelPort | void |  |
| getCnsService | CnsService |  |
| getLatestVersionMemberContract | MemberContract |  |
| getMaxPoolSize | String |  |
| getCorePoolSize | String |  |
| getLatestVersionTableDataSetContract | TableDataSetContract |  |
| getQueueCapacity | String |  |
| getLatestVersionMemberFileInfoContract | MemberFileInfoContract |  |
| getLatestVersionMemberServiceContract | MemberServiceContract |  |
| getCryptoSuite | CryptoSuite |  |
| getLatestVersionImageDataSetContract | ImageDataSetContract |  |
| setCertPath | void |  |
| getLatestVersionDataResourceContract | DataResourceContract |  |
| getGroupId | int |  |
| getLatestContractAddressByName | String |  |
| setMaxPoolSize | void |  |
| getCryptoKeyPair | CryptoKeyPair |  |
| getLatestVersionBloomFilterContract | BloomFilterContract |  |
| setGroupId | void |  |
| getClient | Client |  |
| getBcosSDK | BcosSDK |  |
| getLatestVersionUnionNodeContract | UnionNodeContract |  |
| setCorePoolSize | void |  |
| getLatestVersionDataSetMemberPermissionContract | DataSetMemberPermissionContract |  |
| getLatestVersionDataSetContract | DataSetContract |  |




