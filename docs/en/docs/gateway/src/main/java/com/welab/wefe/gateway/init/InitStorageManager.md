# Basic Information

|      |      |
|------|------|
| Name | InitStorageManager |
| Language | .java |
| Code Path | WeFe/gateway/src/main/java/com/welab/wefe/gateway/init/InitStorageManager.java |
| Package Name | com.welab.wefe.gateway.init |
| Dependencies | ['com.welab.wefe.common.data.storage.service.fc.FcStorage', 'com.welab.wefe.common.data.storage.service.fc.aliyun.AliyunOssConfig', 'com.welab.wefe.common.data.storage.service.fc.tencent.TencentCosConfig', 'com.welab.wefe.common.data.storage.service.persistent.PersistentStorage', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.wefe.dto.global_config.calculation_engine.fc.AliyunFunctionComputeConfigModel', 'com.welab.wefe.common.wefe.dto.global_config.calculation_engine.fc.FunctionComputeBaseConfigModel', 'com.welab.wefe.common.wefe.dto.global_config.calculation_engine.fc.TencentServerlessCloudFunctionConfigModel', 'com.welab.wefe.common.wefe.dto.global_config.storage.ClickHouseStorageConfigModel', 'com.welab.wefe.common.wefe.dto.storage.ClickhouseConfig', 'com.welab.wefe.common.wefe.enums.FcCloudProvider', 'com.welab.wefe.gateway.GatewayServer', 'com.welab.wefe.gateway.service.GlobalConfigService', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.util.concurrent.atomic.AtomicBoolean'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| InitStorageManager | class |  |



## Class InitStorageManager

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | InitStorageManager |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| LOG = LoggerFactory.getLogger(InitStorageManager.class) | Logger |  |
| FC_INIT = new AtomicBoolean(false) | AtomicBoolean |  |
| PERSISTENT_INIT = new AtomicBoolean(false) | AtomicBoolean |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| initPersistent | boolean |  |
| init | void |  |
| initFC | boolean |  |
| initPersistentStorage | boolean |  |
| initFcStorage | boolean |  |




