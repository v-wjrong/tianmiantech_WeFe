# Basic Information

|      |      |
|------|------|
| Name | TransferMetaDataSink |
| Language | .java |
| Code Path | WeFe/gateway/src/main/java/com/welab/wefe/gateway/service/TransferMetaDataSink.java |
| Package Name | com.welab.wefe.gateway.service |
| Dependencies | ['com.welab.wefe.common.util.FileUtil', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.util.ThreadUtil', 'com.welab.wefe.gateway.api.meta.basic.GatewayMetaProto', 'com.welab.wefe.gateway.config.ConfigProperties', 'com.welab.wefe.gateway.service.base.AbstractTransferMetaDataSink', 'com.welab.wefe.gateway.util.SerializeUtil', 'org.apache.commons.collections4.CollectionUtils', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.stereotype.Service', 'java.io.File', 'java.util.ArrayList', 'java.util.List', 'java.util.Map', 'java.util.concurrent.ConcurrentHashMap', 'java.util.concurrent.ConcurrentSkipListSet'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| TransferMetaDataSink | class |  |



## Class TransferMetaDataSink

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | TransferMetaDataSink |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
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

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| sinkTransferMetaDataBaseDir | String |  |
| loadSerializeTransferMetaData | boolean |  |
| tempSaveTransferMetaData | boolean |  |
| sink | void |  |
| startProcessTransferMetaCacheThread | void |  |
| clearTransferMetaDataCache | void |  |
| putProcessingTransferMetaDataCache | void |  |




