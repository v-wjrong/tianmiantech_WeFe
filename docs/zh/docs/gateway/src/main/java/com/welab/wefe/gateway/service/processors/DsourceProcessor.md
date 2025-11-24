# 基础信息

|      |      |
|------|------|
| 名称 | DsourceProcessor |
| 编码语言 | .java |
| 代码路径 | WeFe/gateway/src/main/java/com/welab/wefe/gateway/service/processors/DsourceProcessor.java |
| 包名 | com.welab.wefe.gateway.service.processors |
| 依赖项 | ['com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.wefe.enums.GatewayProcessorType', 'com.welab.wefe.gateway.GatewayServer', 'com.welab.wefe.gateway.api.meta.basic.BasicMetaProto', 'com.welab.wefe.gateway.api.meta.basic.GatewayMetaProto', 'com.welab.wefe.gateway.base.Processor', 'com.welab.wefe.gateway.cache.SendTransferMetaCache', 'com.welab.wefe.gateway.common.ReturnStatusBuilder', 'com.welab.wefe.gateway.common.ReturnStatusEnum', 'com.welab.wefe.gateway.common.StorageConstant', 'com.welab.wefe.gateway.service.MessageService', 'com.welab.wefe.gateway.service.TransferMetaDataSourceParallelStream', 'com.welab.wefe.gateway.service.TransferMetaDataSourceStream', 'com.welab.wefe.gateway.service.base.AbstractSendTransferMetaCachePersistentService', 'com.welab.wefe.gateway.service.base.AbstractTransferMetaDataSink', 'com.welab.wefe.gateway.service.base.AbstractTransferMetaDataSource', 'com.welab.wefe.gateway.util.TransferMetaUtil', 'org.springframework.beans.factory.annotation.Autowired'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| DsourceProcessor | class |  |



## 类 DsourceProcessor

|      |      |
|------|------|
| 访问范围 | @Processor(type = GatewayProcessorType.dSourceProcessor, desc = "Forwarding big data transmission processor (such as CK database data)");public |
| 类型 | class |
| 名称 | DsourceProcessor |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| transferMetaDataSink | AbstractTransferMetaDataSink |  |
| transferMetaDataSource | TransferMetaDataSourceStream |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| pushStreamDateToRemote | BasicMetaProto.ReturnStatus |  |
| recvStreamDateHandle | void |  |
| beforeSendToRemote | BasicMetaProto.ReturnStatus |  |




