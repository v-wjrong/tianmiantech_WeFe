# 基础信息

|      |      |
|------|------|
| 名称 | GrpcServerContext |
| 编码语言 | .java |
| 代码路径 | WeFe/gateway/src/main/java/com/welab/wefe/gateway/init/grpc/GrpcServerContext.java |
| 包名 | com.welab.wefe.gateway.init.grpc |
| 依赖项 | ['java.security.PrivateKey', 'java.security.cert.X509Certificate', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'com.webank.cert.toolkit.utils.CertUtils', 'com.webank.cert.toolkit.utils.KeyUtils', 'com.welab.wefe.common.util.AESUtil', 'com.welab.wefe.common.wefe.dto.global_config.ServerCertInfoModel', 'com.welab.wefe.gateway.GatewayServer', 'com.welab.wefe.gateway.cache.MemberCache', 'com.welab.wefe.gateway.common.GrpcServerScopeEnum', 'com.welab.wefe.gateway.config.ConfigProperties', 'com.welab.wefe.gateway.service.MemberService', 'com.welab.wefe.gateway.service.ServerCertService', 'io.grpc.netty.GrpcSslContexts', 'io.netty.handler.ssl.SslContext', 'io.netty.handler.ssl.SslContextBuilder', 'io.netty.handler.ssl.SslProvider'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| GrpcServerContext | class |  |



## 类 GrpcServerContext

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | GrpcServerContext |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| LOG = LoggerFactory.getLogger(GrpcServerContext.class) | Logger |  |
| internalGrpcServer | GrpcServer |  |
| context = new GrpcServerContext() | GrpcServerContext |  |
| externalGrpcServer | GrpcServer |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getInstance | GrpcServerContext |  |
| buildInternalGrpcServer | GrpcServer |  |
| restartExternalGrpcServer | boolean |  |
| start | boolean |  |
| buildExternalGrpcServer | GrpcServer |  |
| buildSslContext | SslContext |  |
| getExternalGrpcServer | GrpcServer |  |




