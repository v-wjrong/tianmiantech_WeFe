# Basic Information

|      |      |
|------|------|
| Name | AbstractSendTransferMetaService |
| Language | .java |
| Code Path | WeFe/gateway/src/main/java/com/welab/wefe/gateway/service/base/AbstractSendTransferMetaService.java |
| Package Name | com.welab.wefe.gateway.service.base |
| Dependencies | ['com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.wefe.dto.global_config.GatewayConfigModel', 'com.welab.wefe.gateway.api.meta.basic.BasicMetaProto', 'com.welab.wefe.gateway.api.meta.basic.GatewayMetaProto', 'com.welab.wefe.gateway.cache.MemberCache', 'com.welab.wefe.gateway.cache.PartnerConfigCache', 'com.welab.wefe.gateway.common.EndpointBuilder', 'com.welab.wefe.gateway.common.ReturnStatusBuilder', 'com.welab.wefe.gateway.common.ReturnStatusEnum', 'com.welab.wefe.gateway.entity.MemberEntity', 'com.welab.wefe.gateway.entity.PartnerConfigEntity', 'com.welab.wefe.gateway.service.GlobalConfigService', 'com.welab.wefe.gateway.service.MessageService', 'com.welab.wefe.gateway.util.GrpcUtil', 'com.welab.wefe.gateway.util.ReturnStatusUtil', 'com.welab.wefe.gateway.util.TransferMetaUtil', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.beans.factory.annotation.Autowired'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| AbstractSendTransferMetaService | class |  |



## Class AbstractSendTransferMetaService

|      |      |
|------|------|
| Access Modifier | public abstract |
| Type | class |
| Name | AbstractSendTransferMetaService |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| globalConfigService | GlobalConfigService |  |
| messageService | MessageService |  |
| LOG = LoggerFactory.getLogger(this.getClass()) | Logger |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| setDstMemberInfo | GatewayMetaProto.Member |  |
| setMemberInfo | GatewayMetaProto.TransferMeta |  |
| pushToRemote | BasicMetaProto.ReturnStatus |  |
| doHandleCache | BasicMetaProto.ReturnStatus |  |
| doHandle | BasicMetaProto.ReturnStatus |  |
| checkCommonReqParam | BasicMetaProto.ReturnStatus |  |
| send | BasicMetaProto.ReturnStatus |  |




