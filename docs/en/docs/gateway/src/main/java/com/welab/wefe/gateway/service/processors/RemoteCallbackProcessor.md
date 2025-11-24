# Basic Information

|      |      |
|------|------|
| Name | RemoteCallbackProcessor |
| Language | .java |
| Code Path | WeFe/gateway/src/main/java/com/welab/wefe/gateway/service/processors/RemoteCallbackProcessor.java |
| Package Name | com.welab.wefe.gateway.service.processors |
| Dependencies | ['com.welab.wefe.common.wefe.enums.GatewayProcessorType', 'com.welab.wefe.gateway.api.meta.basic.BasicMetaProto', 'com.welab.wefe.gateway.api.meta.basic.GatewayMetaProto', 'com.welab.wefe.gateway.base.Processor', 'com.welab.wefe.gateway.service.MessageService', 'org.springframework.beans.factory.annotation.Autowired'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| RemoteCallbackProcessor | class |  |



## Class RemoteCallbackProcessor

|      |      |
|------|------|
| Access Modifier | @Processor(type = GatewayProcessorType.remoteCallbackProcessor, desc = "Notify the other party of an error message");public |
| Type | class |
| Name | RemoteCallbackProcessor |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| messageService | MessageService |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| remoteProcess | BasicMetaProto.ReturnStatus |  |




