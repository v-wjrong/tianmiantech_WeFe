# Basic Information

|      |      |
|------|------|
| Name | BlockchainConfig |
| Language | .java |
| Code Path | WeFe/union/blockchain-data-sync/src/main/java/com/welab/wefe/config/BlockchainConfig.java |
| Package Name | com.welab.wefe.config |
| Dependencies | ['io.netty.channel.ChannelHandlerContext', 'org.fisco.bcos.sdk.BcosSDK', 'org.fisco.bcos.sdk.config.ConfigOption', 'org.fisco.bcos.sdk.config.exceptions.ConfigException', 'org.fisco.bcos.sdk.config.model.ConfigProperty', 'org.fisco.bcos.sdk.model.Message', 'org.fisco.bcos.sdk.network.MsgHandler', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.boot.context.properties.ConfigurationProperties', 'org.springframework.context.annotation.Bean', 'org.springframework.context.annotation.Configuration', 'java.util.ArrayList', 'java.util.HashMap', 'java.util.List', 'java.util.Map'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| BlockchainConfig | class |  |



## Class BlockchainConfig

|      |      |
|------|------|
| Access Modifier | @Configuration;@ConfigurationProperties(prefix = "sdk");public |
| Type | class |
| Name | BlockchainConfig |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| queueCapacity | String |  |
| log =            LoggerFactory.getLogger(BlockchainConfig.class) | Logger |  |
| ip = "127.0.0.1" | String |  |
| corePoolSize | String |  |
| maxPoolSize | String |  |
| channelPort = "20200" | String |  |
| groupIdList | List<Integer> |  |
| certPath = "conf" | String |  |
| PEER_CONNECTED = true | boolean |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getBcosSDK | BcosSDK |  |
| setGroupIdList | void |  |
| getCorePoolSize | String |  |
| getCertPath | String |  |
| setMaxPoolSize | void |  |
| setQueueCapacity | void |  |
| getMaxPoolSize | String |  |
| setCorePoolSize | void |  |
| getGroupIdList | List<Integer> |  |
| setCertPath | void |  |
| getQueueCapacity | String |  |
| getIp | String |  |
| setIp | void |  |
| getChannelPort | String |  |
| setChannelPort | void |  |




