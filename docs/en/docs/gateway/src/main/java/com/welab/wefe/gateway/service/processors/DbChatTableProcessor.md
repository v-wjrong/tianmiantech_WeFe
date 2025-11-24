# Basic Information

|      |      |
|------|------|
| Name | DbChatTableProcessor |
| Language | .java |
| Code Path | WeFe/gateway/src/main/java/com/welab/wefe/gateway/service/processors/DbChatTableProcessor.java |
| Package Name | com.welab.wefe.gateway.service.processors |
| Dependencies | ['com.welab.wefe.common.wefe.enums.GatewayProcessorType', 'com.welab.wefe.common.wefe.enums.ProducerType', 'com.welab.wefe.gateway.GatewayServer', 'com.welab.wefe.gateway.api.meta.basic.BasicMetaProto', 'com.welab.wefe.gateway.api.meta.basic.GatewayMetaProto', 'com.welab.wefe.gateway.base.Processor', 'com.welab.wefe.gateway.common.ReturnStatusBuilder', 'com.welab.wefe.gateway.entity.MessageQueueEntity', 'com.welab.wefe.gateway.service.MessageQueueService'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| DbChatTableProcessor | class |  |



## Class DbChatTableProcessor

|      |      |
|------|------|
| Access Modifier | @Processor(type = GatewayProcessorType.dbChatTableProcessor, desc = "The message is saved to the exchange center queue list processor of MySQL");public |
| Type | class |
| Name | DbChatTableProcessor |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| save | void |  |
| remoteProcess | BasicMetaProto.ReturnStatus |  |




