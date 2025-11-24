# 基础信息

|      |      |
|------|------|
| 名称 | DbChatTableProcessor |
| 编码语言 | .java |
| 代码路径 | WeFe/gateway/src/main/java/com/welab/wefe/gateway/service/processors/DbChatTableProcessor.java |
| 包名 | com.welab.wefe.gateway.service.processors |
| 依赖项 | ['com.welab.wefe.common.wefe.enums.GatewayProcessorType', 'com.welab.wefe.common.wefe.enums.ProducerType', 'com.welab.wefe.gateway.GatewayServer', 'com.welab.wefe.gateway.api.meta.basic.BasicMetaProto', 'com.welab.wefe.gateway.api.meta.basic.GatewayMetaProto', 'com.welab.wefe.gateway.base.Processor', 'com.welab.wefe.gateway.common.ReturnStatusBuilder', 'com.welab.wefe.gateway.entity.MessageQueueEntity', 'com.welab.wefe.gateway.service.MessageQueueService'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| DbChatTableProcessor | class |  |



## 类 DbChatTableProcessor

|      |      |
|------|------|
| 访问范围 | @Processor(type = GatewayProcessorType.dbChatTableProcessor, desc = "The message is saved to the exchange center queue list processor of MySQL");public |
| 类型 | class |
| 名称 | DbChatTableProcessor |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| save | void |  |
| remoteProcess | BasicMetaProto.ReturnStatus |  |




