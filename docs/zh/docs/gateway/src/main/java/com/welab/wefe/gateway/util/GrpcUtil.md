# 基础信息

|      |      |
|------|------|
| 名称 | GrpcUtil |
| 编码语言 | .java |
| 代码路径 | WeFe/gateway/src/main/java/com/welab/wefe/gateway/util/GrpcUtil.java |
| 包名 | com.welab.wefe.gateway.util |
| 依赖项 | ['java.security.cert.X509Certificate', 'java.util.Arrays', 'java.util.Date', 'java.util.List', 'java.util.concurrent.TimeUnit', 'javax.net.ssl.SSLException', 'com.welab.wefe.gateway.cache.PartnerConfigCache', 'org.apache.commons.lang3.math.NumberUtils', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'com.google.protobuf.MessageOrBuilder', 'com.google.protobuf.util.JsonFormat', 'com.welab.wefe.common.util.DateUtil', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.util.ThreadUtil', 'com.welab.wefe.gateway.api.meta.basic.BasicMetaProto', 'com.welab.wefe.gateway.api.meta.basic.GatewayMetaProto', 'com.welab.wefe.gateway.api.service.proto.NetworkDataTransferProxyServiceGrpc', 'com.welab.wefe.gateway.cache.GrpcChannelCache', 'com.welab.wefe.gateway.cache.MemberCache', 'com.welab.wefe.gateway.common.EndpointBuilder', 'com.welab.wefe.gateway.common.GrpcConstant', 'com.welab.wefe.gateway.common.ReturnStatusBuilder', 'com.welab.wefe.gateway.entity.MemberEntity', 'com.welab.wefe.gateway.interceptor.AntiTamperMetadataBuilder', 'com.welab.wefe.gateway.interceptor.ClientCallCredentials', 'com.welab.wefe.gateway.interceptor.SignVerifyMetadataBuilder', 'com.welab.wefe.gateway.interceptor.SystemTimestampMetadataBuilder', 'io.grpc.ManagedChannel', 'io.grpc.ManagedChannelBuilder', 'io.grpc.StatusRuntimeException', 'io.grpc.netty.GrpcSslContexts', 'io.grpc.netty.NegotiationType', 'io.grpc.netty.NettyChannelBuilder', 'io.netty.handler.ssl.SslContextBuilder', 'io.netty.handler.ssl.util.InsecureTrustManagerFactory'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| GrpcUtil | class |  |



## 类 GrpcUtil

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | GrpcUtil |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| LOG = LoggerFactory.getLogger(GrpcUtil.class) | Logger |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| pushToRemote | BasicMetaProto.ReturnStatus |  |
| getSslManagedChannel | ManagedChannel |  |
| checkIsConnectionDisableExp | boolean |  |
| checkIsSignPermissionExp | boolean |  |
| getSslManagedChannel | ManagedChannel |  |
| getManagedChannel | ManagedChannel |  |
| toJsonString | String |  |
| getMessageProtobufferByte | byte[] |  |
| checkIsSslConnectionDisableExp | boolean |  |
| checkSystemTimestampPermissionExp | boolean |  |
| getManagedChannel | ManagedChannel |  |
| checkAntiTamperExp | boolean |  |
| checkIsIpPermissionExp | boolean |  |
| checkGatewayUriValid | boolean |  |
| closeManagedChannel | void |  |
| checkTlsEnable | boolean |  |




