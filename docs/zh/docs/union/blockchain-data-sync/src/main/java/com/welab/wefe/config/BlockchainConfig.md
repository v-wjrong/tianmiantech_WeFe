# 基础信息

|      |      |
|------|------|
| 名称 | BlockchainConfig |
| 编码语言 | .java |
| 代码路径 | WeFe/union/blockchain-data-sync/src/main/java/com/welab/wefe/config/BlockchainConfig.java |
| 包名 | com.welab.wefe.config |
| 依赖项 | ['io.netty.channel.ChannelHandlerContext', 'org.fisco.bcos.sdk.BcosSDK', 'org.fisco.bcos.sdk.config.ConfigOption', 'org.fisco.bcos.sdk.config.exceptions.ConfigException', 'org.fisco.bcos.sdk.config.model.ConfigProperty', 'org.fisco.bcos.sdk.model.Message', 'org.fisco.bcos.sdk.network.MsgHandler', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.boot.context.properties.ConfigurationProperties', 'org.springframework.context.annotation.Bean', 'org.springframework.context.annotation.Configuration', 'java.util.ArrayList', 'java.util.HashMap', 'java.util.List', 'java.util.Map'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| BlockchainConfig | class |  |



## 类 BlockchainConfig

|      |      |
|------|------|
| 访问范围 | @Configuration;@ConfigurationProperties(prefix = "sdk");public |
| 类型 | class |
| 名称 | BlockchainConfig |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
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

### 方法列表

| 名称  | 类型  | 说明 |
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




