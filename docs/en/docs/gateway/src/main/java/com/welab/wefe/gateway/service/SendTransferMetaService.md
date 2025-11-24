# Basic Information

|      |      |
|------|------|
| Name | SendTransferMetaService |
| Language | .java |
| Code Path | WeFe/gateway/src/main/java/com/welab/wefe/gateway/service/SendTransferMetaService.java |
| Package Name | com.welab.wefe.gateway.service |
| Dependencies | ['com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.gateway.api.meta.basic.BasicMetaProto', 'com.welab.wefe.gateway.api.meta.basic.GatewayMetaProto', 'com.welab.wefe.gateway.common.ReturnStatusBuilder', 'com.welab.wefe.gateway.service.base.AbstractSendTransferMetaCachePersistentService', 'com.welab.wefe.gateway.service.base.AbstractSendTransferMetaService', 'com.welab.wefe.gateway.service.processors.DsourceProcessor', 'com.welab.wefe.gateway.service.processors.ProcessorContext', 'com.welab.wefe.gateway.util.ReturnStatusUtil', 'com.welab.wefe.gateway.util.TransferMetaUtil', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.stereotype.Service'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| SendTransferMetaService | class |  |



## Class SendTransferMetaService

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | SendTransferMetaService |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| mMessageService | MessageService |  |
| sendTransferMetaCachePersistentService | AbstractSendTransferMetaCachePersistentService |  |
| LOG = LoggerFactory.getLogger(SendTransferMetaService.class) | Logger |  |
| dsourceProcessor | DsourceProcessor |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| doHandle | BasicMetaProto.ReturnStatus |  |
| doHandleCache | BasicMetaProto.ReturnStatus |  |




