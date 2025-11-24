# Basic Information

|      |      |
|------|------|
| Name | GrpcChannelCache |
| Language | .java |
| Code Path | WeFe/gateway/src/main/java/com/welab/wefe/gateway/cache/GrpcChannelCache.java |
| Package Name | com.welab.wefe.gateway.cache |
| Dependencies | ['com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.gateway.common.EndpointBuilder', 'com.welab.wefe.gateway.util.GrpcUtil', 'io.grpc.ManagedChannel', 'net.jodah.expiringmap.ExpirationListener', 'net.jodah.expiringmap.ExpirationPolicy', 'net.jodah.expiringmap.ExpiringMap', 'javax.net.ssl.SSLException', 'java.security.cert.X509Certificate', 'java.util.concurrent.TimeUnit'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| GrpcChannelCache | class |  |



## Class GrpcChannelCache

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | GrpcChannelCache |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| LOCK = new Object() | Object |  |
| CHANNEL_CACHE = new GrpcChannelCache() | GrpcChannelCache |  |
| data = ExpiringMap            .builder()            .expirationListener(new MyExpirationListener())            .expirationPolicy(ExpirationPolicy.ACCESSED)            .expiration(24, TimeUnit.HOURS)            .build() | ExpiringMap<String, ChannelInfo> |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getInstance | GrpcChannelCache |  |
| getNonNull | ManagedChannel |  |
| remove | void |  |




