# Basic Information

|      |      |
|------|------|
| Name | TransferMetaDataSource |
| Language | .java |
| Code Path | WeFe/gateway/src/main/java/com/welab/wefe/gateway/service/TransferMetaDataSource.java |
| Package Name | com.welab.wefe.gateway.service |
| Dependencies | ['com.google.common.util.concurrent.SettableFuture', 'com.welab.wefe.common.data.storage.model.DataItemModel', 'com.welab.wefe.common.data.storage.model.PageInputModel', 'com.welab.wefe.common.data.storage.model.PageOutputModel', 'com.welab.wefe.common.data.storage.service.persistent.PersistentStorage', 'com.welab.wefe.common.util.ThreadUtil', 'com.welab.wefe.gateway.api.meta.basic.BasicMetaProto', 'com.welab.wefe.gateway.api.meta.basic.GatewayMetaProto', 'com.welab.wefe.gateway.api.service.proto.NetworkDataTransferProxyServiceGrpc', 'com.welab.wefe.gateway.api.streammessage.PushDataSourceResponseStreamObserver', 'com.welab.wefe.gateway.cache.GrpcChannelCache', 'com.welab.wefe.gateway.cache.MemberCache', 'com.welab.wefe.gateway.common.EndpointBuilder', 'com.welab.wefe.gateway.common.KeyValueDataBuilder', 'com.welab.wefe.gateway.common.ReturnStatusBuilder', 'com.welab.wefe.gateway.config.ConfigProperties', 'com.welab.wefe.gateway.entity.MemberEntity', 'com.welab.wefe.gateway.interceptor.ClientCallCredentials', 'com.welab.wefe.gateway.interceptor.SignVerifyMetadataBuilder', 'com.welab.wefe.gateway.interceptor.SystemTimestampMetadataBuilder', 'com.welab.wefe.gateway.service.base.AbstractTransferMetaDataSource', 'com.welab.wefe.gateway.util.GrpcUtil', 'com.welab.wefe.gateway.util.TlsUtil', 'com.welab.wefe.gateway.util.TransferMetaUtil', 'io.grpc.ManagedChannel', 'io.grpc.StatusRuntimeException', 'io.grpc.stub.StreamObserver', 'org.apache.commons.collections4.CollectionUtils', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.stereotype.Service', 'java.util.ArrayList', 'java.util.List'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| TransferMetaDataSource | class |  |



## Class TransferMetaDataSource

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | TransferMetaDataSource |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| configProperties | ConfigProperties |  |
| PAGE_SIZE_THREAD_LOCAL = new ThreadLocal<>() | ThreadLocal<Integer> |  |
| FAIL_RETRY_COUNT = 20 | int |  |
| OPTIMAL_SUB_BLOCK_SIZE_THREAD_LOCAL = new ThreadLocal<>() | ThreadLocal<Integer> |  |
| LOG = LoggerFactory.getLogger(TransferMetaDataSource.class) | Logger |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| sendCompleteRequest | boolean |  |
| sendBlock | List<GatewayMetaProto.TransferMeta> |  |
| getTotalPage | int |  |
| getBlockSequenceNo | int |  |
| getData | PageOutputModel<byte[], byte[]> |  |
| splitConfigDataList | List<List<BasicMetaProto.KeyValueData>> |  |
| blockSplitToTransferMetaList | List<GatewayMetaProto.TransferMeta> |  |
| wrapData | List<BasicMetaProto.KeyValueData> |  |
| getSplitBlockCount | int |  |
| getSendFailedTransferMetaList | List<GatewayMetaProto.TransferMeta> |  |
| getDataAndPushToRemote | BasicMetaProto.ReturnStatus |  |
| setPagingParams | void |  |
| getTotalTransferMetaBlocks | List<GatewayMetaProto.TransferMeta> |  |
| printSendFailBlocksErrorLog | void |  |
| sendBlockTransferMetaDataListToRemote | List<GatewayMetaProto.TransferMeta> |  |
| clearPagingParams | void |  |




