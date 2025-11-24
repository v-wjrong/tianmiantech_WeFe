# Basic Information

|      |      |
|------|------|
| Name | DbFlowTableProcessor |
| Language | .java |
| Code Path | WeFe/gateway/src/main/java/com/welab/wefe/gateway/service/processors/DbFlowTableProcessor.java |
| Package Name | com.welab.wefe.gateway.service.processors |
| Dependencies | ['com.welab.wefe.common.wefe.enums.GatewayProcessorType', 'com.welab.wefe.common.wefe.enums.ProducerType', 'com.welab.wefe.gateway.GatewayServer', 'com.welab.wefe.gateway.api.meta.basic.BasicMetaProto', 'com.welab.wefe.gateway.api.meta.basic.GatewayMetaProto', 'com.welab.wefe.gateway.base.Processor', 'com.welab.wefe.gateway.common.ReturnStatusBuilder', 'com.welab.wefe.gateway.entity.FlowActionQueueEntity', 'com.welab.wefe.gateway.service.FlowActionQueueService'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| DbFlowTableProcessor | class |  |



## Class DbFlowTableProcessor

|      |      |
|------|------|
| Access Modifier | @Processor(type = GatewayProcessorType.dbFlowTableProcessor, desc = "The message is saved to the flow action queue list processor of MySQL");public |
| Type | class |
| Name | DbFlowTableProcessor |
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




