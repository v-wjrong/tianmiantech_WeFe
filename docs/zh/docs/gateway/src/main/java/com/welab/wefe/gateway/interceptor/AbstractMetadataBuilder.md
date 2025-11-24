# 基础信息

|      |      |
|------|------|
| 名称 | AbstractMetadataBuilder |
| 编码语言 | .java |
| 代码路径 | WeFe/gateway/src/main/java/com/welab/wefe/gateway/interceptor/AbstractMetadataBuilder.java |
| 包名 | com.welab.wefe.gateway.interceptor |
| 依赖项 | ['com.welab.wefe.gateway.api.meta.basic.GatewayMetaProto', 'io.grpc.Metadata', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| AbstractMetadataBuilder | class |  |



## 类 AbstractMetadataBuilder

|      |      |
|------|------|
| 访问范围 | public abstract |
| 类型 | class |
| 名称 | AbstractMetadataBuilder |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| transferMeta | GatewayMetaProto.TransferMeta |  |
| LOG = LoggerFactory.getLogger(this.getClass()) | Logger |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| build | Metadata |  |
| setTransferMeta | void |  |
| getTransferMeta | GatewayMetaProto.TransferMeta |  |




