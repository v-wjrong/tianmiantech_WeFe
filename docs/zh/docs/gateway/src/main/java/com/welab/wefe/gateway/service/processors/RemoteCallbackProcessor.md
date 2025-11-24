# 基础信息

|      |      |
|------|------|
| 名称 | RemoteCallbackProcessor |
| 编码语言 | .java |
| 代码路径 | WeFe/gateway/src/main/java/com/welab/wefe/gateway/service/processors/RemoteCallbackProcessor.java |
| 包名 | com.welab.wefe.gateway.service.processors |
| 依赖项 | ['com.welab.wefe.common.wefe.enums.GatewayProcessorType', 'com.welab.wefe.gateway.api.meta.basic.BasicMetaProto', 'com.welab.wefe.gateway.api.meta.basic.GatewayMetaProto', 'com.welab.wefe.gateway.base.Processor', 'com.welab.wefe.gateway.service.MessageService', 'org.springframework.beans.factory.annotation.Autowired'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| RemoteCallbackProcessor | class |  |



## 类 RemoteCallbackProcessor

|      |      |
|------|------|
| 访问范围 | @Processor(type = GatewayProcessorType.remoteCallbackProcessor, desc = "Notify the other party of an error message");public |
| 类型 | class |
| 名称 | RemoteCallbackProcessor |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| messageService | MessageService |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| remoteProcess | BasicMetaProto.ReturnStatus |  |




