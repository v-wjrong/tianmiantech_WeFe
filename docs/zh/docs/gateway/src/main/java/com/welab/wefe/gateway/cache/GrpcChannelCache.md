# 基础信息

|      |      |
|------|------|
| 名称 | GrpcChannelCache |
| 编码语言 | .java |
| 代码路径 | WeFe/gateway/src/main/java/com/welab/wefe/gateway/cache/GrpcChannelCache.java |
| 包名 | com.welab.wefe.gateway.cache |
| 依赖项 | ['com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.gateway.common.EndpointBuilder', 'com.welab.wefe.gateway.util.GrpcUtil', 'io.grpc.ManagedChannel', 'net.jodah.expiringmap.ExpirationListener', 'net.jodah.expiringmap.ExpirationPolicy', 'net.jodah.expiringmap.ExpiringMap', 'javax.net.ssl.SSLException', 'java.security.cert.X509Certificate', 'java.util.concurrent.TimeUnit'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| GrpcChannelCache | class |  |



## 类 GrpcChannelCache

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | GrpcChannelCache |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| LOCK = new Object() | Object |  |
| CHANNEL_CACHE = new GrpcChannelCache() | GrpcChannelCache |  |
| data = ExpiringMap            .builder()            .expirationListener(new MyExpirationListener())            .expirationPolicy(ExpirationPolicy.ACCESSED)            .expiration(24, TimeUnit.HOURS)            .build() | ExpiringMap<String, ChannelInfo> |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getInstance | GrpcChannelCache |  |
| getNonNull | ManagedChannel |  |
| remove | void |  |




