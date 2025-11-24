# Basic Information

|      |      |
|------|------|
| Name | AbstractCallCredentials |
| Language | .java |
| Code Path | WeFe/gateway/src/main/java/com/welab/wefe/gateway/interceptor/AbstractCallCredentials.java |
| Package Name | com.welab.wefe.gateway.interceptor |
| Dependencies | ['com.welab.wefe.gateway.api.meta.basic.GatewayMetaProto', 'io.grpc.CallCredentials', 'io.grpc.Metadata', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.util.ArrayList', 'java.util.Arrays', 'java.util.List', 'java.util.concurrent.Executor'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| AbstractCallCredentials | class |  |



## Class AbstractCallCredentials

|      |      |
|------|------|
| Access Modifier | public abstract |
| Type | class |
| Name | AbstractCallCredentials |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| LOG = LoggerFactory.getLogger(this.getClass()) | Logger |  |
| metadataBuilders = new ArrayList<>() | List<AbstractMetadataBuilder> |  |
| transferMeta | GatewayMetaProto.TransferMeta |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| thisUsesUnstableApi | void |  |
| applyRequestMetadata | void |  |
| getTransferMeta | GatewayMetaProto.TransferMeta |  |




