# Basic Information

|      |      |
|------|------|
| Name | AbstractMetadataBuilder |
| Language | .java |
| Code Path | WeFe/gateway/src/main/java/com/welab/wefe/gateway/interceptor/AbstractMetadataBuilder.java |
| Package Name | com.welab.wefe.gateway.interceptor |
| Dependencies | ['com.welab.wefe.gateway.api.meta.basic.GatewayMetaProto', 'io.grpc.Metadata', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| AbstractMetadataBuilder | class |  |



## Class AbstractMetadataBuilder

|      |      |
|------|------|
| Access Modifier | public abstract |
| Type | class |
| Name | AbstractMetadataBuilder |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| transferMeta | GatewayMetaProto.TransferMeta |  |
| LOG = LoggerFactory.getLogger(this.getClass()) | Logger |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| build | Metadata |  |
| setTransferMeta | void |  |
| getTransferMeta | GatewayMetaProto.TransferMeta |  |




