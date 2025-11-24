# 基础信息

|      |      |
|------|------|
| 名称 | BlockChainConfig |
| 编码语言 | .java |
| 代码路径 | WeFe/manager/manager-service/src/main/java/com/welab/wefe/manager/service/config/BlockChainConfig.java |
| 包名 | com.welab.wefe.manager.service.config |
| 依赖项 | ['com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.wefe.enums.ContractName', 'com.welab.wefe.manager.service.contract', 'io.netty.channel.ChannelHandlerContext', 'org.apache.commons.collections4.CollectionUtils', 'org.fisco.bcos.sdk.BcosSDK', 'org.fisco.bcos.sdk.client.Client', 'org.fisco.bcos.sdk.config.ConfigOption', 'org.fisco.bcos.sdk.config.model.ConfigProperty', 'org.fisco.bcos.sdk.contract.precompiled.cns.CnsInfo', 'org.fisco.bcos.sdk.contract.precompiled.cns.CnsService', 'org.fisco.bcos.sdk.crypto.CryptoSuite', 'org.fisco.bcos.sdk.crypto.keypair.CryptoKeyPair', 'org.fisco.bcos.sdk.model.Message', 'org.fisco.bcos.sdk.model.NodeVersion.ClientVersion', 'org.fisco.bcos.sdk.network.MsgHandler', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.boot.context.properties.ConfigurationProperties', 'org.springframework.context.annotation.Bean', 'org.springframework.context.annotation.Configuration', 'java.util.ArrayList', 'java.util.HashMap', 'java.util.List', 'java.util.Map'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| BlockChainConfig | class |  |



## 类 BlockChainConfig

|      |      |
|------|------|
| 访问范围 | @Configuration;@ConfigurationProperties(prefix = "block.chain");public |
| 类型 | class |
| 名称 | BlockChainConfig |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| channelPort = "20200" | String |  |
| maxPoolSize | String |  |
| queueCapacity | String |  |
| groupId | int |  |
| certPath = "conf" | String |  |
| corePoolSize | String |  |
| PEER_CONNECTED = true | boolean |  |
| log =            LoggerFactory.getLogger(BlockChainConfig.class) | Logger |  |
| ip = "127.0.0.1" | String |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getCryptoKeyPair | CryptoKeyPair |  |
| getCertPath | String |  |
| getCurrentBlockchainNodeId | String |  |
| getLatestVersionTrustCertsContract | TrustCertsContract |  |
| getClient | Client |  |
| getBcosSDK | BcosSDK |  |
| getQueueCapacity | String |  |
| getLatestVersionMemberContract | MemberContract |  |
| getLatestVersionMemberAuthTypeContract | MemberAuthTypeContract |  |
| getMaxPoolSize | String |  |
| getLatestVersionDataResourceContract | DataResourceContract |  |
| setCertPath | void |  |
| getLatestVersionUnionNodeContract | UnionNodeContract |  |
| setGroupId | void |  |
| getLatestVersionDataSetMemberPermissionContract | DataSetMemberPermissionContract |  |
| setMaxPoolSize | void |  |
| getLatestContractAddressByName | String |  |
| getLatestVersionDataSetContract | DataSetContract |  |
| getLatestVersionRealnameAuthAgreementTemplateContract | RealnameAuthAgreementTemplateContract |  |
| getCnsService | CnsService |  |
| getCorePoolSize | String |  |
| setCorePoolSize | void |  |
| getLatestVersionDataResourceDefaultTagContract | DataResourceDefaultTagContract |  |
| getCryptoSuite | CryptoSuite |  |
| getLatestVersionDataSetDefaultTagContract | DataSetDefaultTagContract |  |
| setQueueCapacity | void |  |
| getIp | String |  |
| setIp | void |  |
| getGroupId | int |  |
| getChannelPort | String |  |
| setChannelPort | void |  |




