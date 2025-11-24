# 基础信息

|      |      |
|------|------|
| 名称 | TransferMetaDataSink |
| 编码语言 | .java |
| 代码路径 | WeFe/gateway/src/main/java/com/welab/wefe/gateway/service/TransferMetaDataSink.java |
| 包名 | com.welab.wefe.gateway.service |
| 依赖项 | ['com.welab.wefe.common.util.FileUtil', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.util.ThreadUtil', 'com.welab.wefe.gateway.api.meta.basic.GatewayMetaProto', 'com.welab.wefe.gateway.config.ConfigProperties', 'com.welab.wefe.gateway.service.base.AbstractTransferMetaDataSink', 'com.welab.wefe.gateway.util.SerializeUtil', 'org.apache.commons.collections4.CollectionUtils', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.stereotype.Service', 'java.io.File', 'java.util.ArrayList', 'java.util.List', 'java.util.Map', 'java.util.concurrent.ConcurrentHashMap', 'java.util.concurrent.ConcurrentSkipListSet'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| TransferMetaDataSink | class |  |



## 类 TransferMetaDataSink

|      |      |
|------|------|
| 访问范围 | @Service;public |
| 类型 | class |
| 名称 | TransferMetaDataSink |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| SINK_TEMP_DIR_NAME = "sink" | String |  |
| configProperties | ConfigProperties |  |
| processingTransferMetaDataCache = new ConcurrentHashMap<>() | ConcurrentHashMap<String, ConcurrentSkipListSet<ProcessingTransferMetaData>> |  |
| messageService | MessageService |  |
| LOG = LoggerFactory.getLogger(TransferMetaDataSink.class) | Logger |  |
| completeBlockFlagCache = new ConcurrentHashMap<>() | ConcurrentHashMap<String, GatewayMetaProto.TransferMeta> |  |
| PROCESS_STATUS_SUCCESS = 1 | int |  |
| PROCESS_STATUS_ING = 0 | int |  |
| transferMetaDataAsyncSaveService | TransferMetaDataAsyncSaveService |  |
| PROCESS_STATUS_FAIL = 2 | int |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| sinkTransferMetaDataBaseDir | String |  |
| loadSerializeTransferMetaData | boolean |  |
| tempSaveTransferMetaData | boolean |  |
| sink | void |  |
| startProcessTransferMetaCacheThread | void |  |
| clearTransferMetaDataCache | void |  |
| putProcessingTransferMetaDataCache | void |  |




