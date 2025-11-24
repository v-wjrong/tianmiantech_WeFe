# Basic Information

|      |      |
|------|------|
| Name | BaseGatewayService |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/BaseGatewayService.java |
| Package Name | com.welab.wefe.board.service.service |
| Dependencies | ['com.alibaba.fastjson.JSON', 'com.alibaba.fastjson.JSONObject', 'com.google.protobuf.MessageOrBuilder', 'com.google.protobuf.util.JsonFormat', 'com.welab.wefe.board.service.cache.CaCertificateCache', 'com.welab.wefe.board.service.proto.TransferServiceGrpc', 'com.welab.wefe.board.service.proto.meta.basic.BasicMetaProto', 'com.welab.wefe.board.service.proto.meta.basic.GatewayMetaProto', 'com.welab.wefe.board.service.service.globalconfig.GlobalConfigService', 'com.welab.wefe.board.service.util.TlsUtil', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.wefe.dto.global_config.GatewayConfigModel', 'com.welab.wefe.common.wefe.enums.GatewayProcessorType', 'io.grpc.ManagedChannel', 'io.grpc.ManagedChannelBuilder', 'io.grpc.netty.GrpcSslContexts', 'io.grpc.netty.NegotiationType', 'io.grpc.netty.NettyChannelBuilder', 'io.netty.handler.ssl.SslContextBuilder', 'io.netty.handler.ssl.util.InsecureTrustManagerFactory', 'org.apache.commons.lang3.math.NumberUtils', 'org.springframework.beans.factory.annotation.Autowired', 'java.security.cert.X509Certificate', 'java.util.UUID', 'java.util.concurrent.TimeUnit'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| BaseGatewayService | class |  |



## Class BaseGatewayService

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | BaseGatewayService |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| globalConfigService | GlobalConfigService |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| callGateway | JSONObject |  |
| sendToMyselfGateway | JSONObject |  |
| sendToOtherGateway | JSONObject |  |
| checkPermission | void |  |
| transferMetaToString | String |  |
| sendToMyselfGateway | JSONObject |  |
| getGrpcChannel | ManagedChannel |  |
| sendToOtherGateway | JSONObject |  |
| buildTransferMeta | GatewayMetaProto.TransferMeta |  |
| isValidGatewayUri | boolean |  |
| buildManagedChannel | ManagedChannel |  |
| getSslGrpcChannel | ManagedChannel |  |




