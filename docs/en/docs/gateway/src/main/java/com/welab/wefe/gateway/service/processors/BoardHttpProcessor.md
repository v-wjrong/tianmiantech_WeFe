# Basic Information

|      |      |
|------|------|
| Name | BoardHttpProcessor |
| Language | .java |
| Code Path | WeFe/gateway/src/main/java/com/welab/wefe/gateway/service/processors/BoardHttpProcessor.java |
| Package Name | com.welab.wefe.gateway.service.processors |
| Dependencies | ['java.util.HashMap', 'java.util.Map', 'org.springframework.beans.factory.annotation.Autowired', 'com.welab.wefe.common.http.HttpResponse', 'com.welab.wefe.common.util.AsymmetricCryptoUtil', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.util.SM4Util', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.wefe.dto.global_config.BoardConfigModel', 'com.welab.wefe.common.wefe.enums.GatewayProcessorType', 'com.welab.wefe.gateway.api.meta.basic.BasicMetaProto', 'com.welab.wefe.gateway.api.meta.basic.GatewayMetaProto', 'com.welab.wefe.gateway.base.Processor', 'com.welab.wefe.gateway.cache.MemberCache', 'com.welab.wefe.gateway.common.ReturnStatusBuilder', 'com.welab.wefe.gateway.config.ConfigProperties', 'com.welab.wefe.gateway.entity.MemberEntity', 'com.welab.wefe.gateway.sdk.BoardHelper', 'com.welab.wefe.gateway.service.GlobalConfigService'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| BoardHttpProcessor | class |  |



## Class BoardHttpProcessor

|      |      |
|------|------|
| Access Modifier | @Processor(type = GatewayProcessorType.boardHttpProcessor, desc = "push to the board module message processor in HTTP mode");public |
| Type | class |
| Name | BoardHttpProcessor |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| config | ConfigProperties |  |
| globalConfigService | GlobalConfigService |  |
| NON_ENCRYPT_MARK_PREFIX = "NON_ENCRYPT:" | String |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| remoteProcess | BasicMetaProto.ReturnStatus |  |
| beforeSendToRemote | BasicMetaProto.ReturnStatus |  |
| encryptTransferMeta | GatewayMetaProto.TransferMeta |  |
| decryptContent | String |  |




