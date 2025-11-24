# Basic Information

|      |      |
|------|------|
| Name | GrpcServerContext |
| Language | .java |
| Code Path | WeFe/gateway/src/main/java/com/welab/wefe/gateway/init/grpc/GrpcServerContext.java |
| Package Name | com.welab.wefe.gateway.init.grpc |
| Dependencies | ['java.security.PrivateKey', 'java.security.cert.X509Certificate', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'com.webank.cert.toolkit.utils.CertUtils', 'com.webank.cert.toolkit.utils.KeyUtils', 'com.welab.wefe.common.util.AESUtil', 'com.welab.wefe.common.wefe.dto.global_config.ServerCertInfoModel', 'com.welab.wefe.gateway.GatewayServer', 'com.welab.wefe.gateway.cache.MemberCache', 'com.welab.wefe.gateway.common.GrpcServerScopeEnum', 'com.welab.wefe.gateway.config.ConfigProperties', 'com.welab.wefe.gateway.service.MemberService', 'com.welab.wefe.gateway.service.ServerCertService', 'io.grpc.netty.GrpcSslContexts', 'io.netty.handler.ssl.SslContext', 'io.netty.handler.ssl.SslContextBuilder', 'io.netty.handler.ssl.SslProvider'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| GrpcServerContext | class |  |



## Class GrpcServerContext

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | GrpcServerContext |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| LOG = LoggerFactory.getLogger(GrpcServerContext.class) | Logger |  |
| internalGrpcServer | GrpcServer |  |
| context = new GrpcServerContext() | GrpcServerContext |  |
| externalGrpcServer | GrpcServer |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getInstance | GrpcServerContext |  |
| buildInternalGrpcServer | GrpcServer |  |
| restartExternalGrpcServer | boolean |  |
| start | boolean |  |
| buildExternalGrpcServer | GrpcServer |  |
| buildSslContext | SslContext |  |
| getExternalGrpcServer | GrpcServer |  |




