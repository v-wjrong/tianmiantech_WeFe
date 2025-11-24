# 基础信息

|      |      |
|------|------|
| 名称 | AbstractCallCredentials |
| 编码语言 | .java |
| 代码路径 | WeFe/gateway/src/main/java/com/welab/wefe/gateway/interceptor/AbstractCallCredentials.java |
| 包名 | com.welab.wefe.gateway.interceptor |
| 依赖项 | ['com.welab.wefe.gateway.api.meta.basic.GatewayMetaProto', 'io.grpc.CallCredentials', 'io.grpc.Metadata', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.util.ArrayList', 'java.util.Arrays', 'java.util.List', 'java.util.concurrent.Executor'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| AbstractCallCredentials | class |  |



## 类 AbstractCallCredentials

|      |      |
|------|------|
| 访问范围 | public abstract |
| 类型 | class |
| 名称 | AbstractCallCredentials |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| LOG = LoggerFactory.getLogger(this.getClass()) | Logger |  |
| metadataBuilders = new ArrayList<>() | List<AbstractMetadataBuilder> |  |
| transferMeta | GatewayMetaProto.TransferMeta |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| thisUsesUnstableApi | void |  |
| applyRequestMetadata | void |  |
| getTransferMeta | GatewayMetaProto.TransferMeta |  |




