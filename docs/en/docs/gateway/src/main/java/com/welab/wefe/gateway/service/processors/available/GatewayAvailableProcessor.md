# Basic Information

|      |      |
|------|------|
| Name | GatewayAvailableProcessor |
| Language | .java |
| Code Path | WeFe/gateway/src/main/java/com/welab/wefe/gateway/service/processors/available/GatewayAvailableProcessor.java |
| Package Name | com.welab.wefe.gateway.service.processors.available |
| Dependencies | ['com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.wefe.checkpoint.AbstractCheckpoint', 'com.welab.wefe.common.wefe.checkpoint.CheckpointManager', 'com.welab.wefe.common.wefe.checkpoint.dto.ServiceAvailableCheckOutput', 'com.welab.wefe.common.wefe.enums.GatewayProcessorType', 'com.welab.wefe.common.wefe.enums.ServiceType', 'com.welab.wefe.gateway.api.meta.basic.BasicMetaProto', 'com.welab.wefe.gateway.api.meta.basic.GatewayMetaProto', 'com.welab.wefe.gateway.base.Processor', 'com.welab.wefe.gateway.common.ReturnStatusBuilder', 'com.welab.wefe.gateway.service.processors.AbstractProcessor', 'com.welab.wefe.gateway.service.processors.available.checkpoint', 'org.springframework.beans.factory.annotation.Autowired', 'java.util.Arrays', 'java.util.List'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| GatewayAvailableProcessor | class |  |



## Class GatewayAvailableProcessor

|      |      |
|------|------|
| Access Modifier | @Processor(type = GatewayProcessorType.gatewayAvailableProcessor, desc = "Gateway availability processor");public |
| Type | class |
| Name | GatewayAvailableProcessor |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| CHECKPOINT_LIST = Arrays.asList(            MysqlCheckpoint.class,            StorageCheckpoint.class,            UnionCheckpoint.class,            BoardCheckpoint.class,            FileSystemCheckpoint.class    ) | List<Class<? extends AbstractCheckpoint>> |  |
| checkpointManager | CheckpointManager |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| beforeSendToRemote | BasicMetaProto.ReturnStatus |  |
| remoteProcess | BasicMetaProto.ReturnStatus |  |




