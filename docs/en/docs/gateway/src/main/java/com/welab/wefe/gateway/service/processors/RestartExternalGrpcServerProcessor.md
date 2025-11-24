# Basic Information

|      |      |
|------|------|
| Name | RestartExternalGrpcServerProcessor |
| Language | .java |
| Code Path | WeFe/gateway/src/main/java/com/welab/wefe/gateway/service/processors/RestartExternalGrpcServerProcessor.java |
| Package Name | com.welab.wefe.gateway.service.processors |
| Dependencies | ['com.welab.wefe.common.wefe.enums.GatewayProcessorType', 'com.welab.wefe.gateway.api.meta.basic.BasicMetaProto', 'com.welab.wefe.gateway.api.meta.basic.GatewayMetaProto', 'com.welab.wefe.gateway.base.Processor', 'com.welab.wefe.gateway.common.ReturnStatusBuilder', 'com.welab.wefe.gateway.common.RpcServerStatusEnum', 'com.welab.wefe.gateway.init.grpc.GrpcServer', 'com.welab.wefe.gateway.init.grpc.GrpcServerContext', 'com.welab.wefe.gateway.service.MemberService', 'org.springframework.beans.factory.annotation.Autowired'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| RestartExternalGrpcServerProcessor | class |  |



## Class RestartExternalGrpcServerProcessor

|      |      |
|------|------|
| Access Modifier | @Processor(type = GatewayProcessorType.restartExternalGrpcServer, desc = "Restart external grpc server processor");public |
| Type | class |
| Name | RestartExternalGrpcServerProcessor |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| memberService | MemberService |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| beforeSendToRemote | BasicMetaProto.ReturnStatus |  |




