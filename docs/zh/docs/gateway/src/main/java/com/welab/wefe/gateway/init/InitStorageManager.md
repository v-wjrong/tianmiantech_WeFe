# 基础信息

|      |      |
|------|------|
| 名称 | InitStorageManager |
| 编码语言 | .java |
| 代码路径 | WeFe/gateway/src/main/java/com/welab/wefe/gateway/init/InitStorageManager.java |
| 包名 | com.welab.wefe.gateway.init |
| 依赖项 | ['com.welab.wefe.common.data.storage.service.fc.FcStorage', 'com.welab.wefe.common.data.storage.service.fc.aliyun.AliyunOssConfig', 'com.welab.wefe.common.data.storage.service.fc.tencent.TencentCosConfig', 'com.welab.wefe.common.data.storage.service.persistent.PersistentStorage', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.wefe.dto.global_config.calculation_engine.fc.AliyunFunctionComputeConfigModel', 'com.welab.wefe.common.wefe.dto.global_config.calculation_engine.fc.FunctionComputeBaseConfigModel', 'com.welab.wefe.common.wefe.dto.global_config.calculation_engine.fc.TencentServerlessCloudFunctionConfigModel', 'com.welab.wefe.common.wefe.dto.global_config.storage.ClickHouseStorageConfigModel', 'com.welab.wefe.common.wefe.dto.storage.ClickhouseConfig', 'com.welab.wefe.common.wefe.enums.FcCloudProvider', 'com.welab.wefe.gateway.GatewayServer', 'com.welab.wefe.gateway.service.GlobalConfigService', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.util.concurrent.atomic.AtomicBoolean'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| InitStorageManager | class |  |



## 类 InitStorageManager

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | InitStorageManager |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| LOG = LoggerFactory.getLogger(InitStorageManager.class) | Logger |  |
| FC_INIT = new AtomicBoolean(false) | AtomicBoolean |  |
| PERSISTENT_INIT = new AtomicBoolean(false) | AtomicBoolean |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| initPersistent | boolean |  |
| init | void |  |
| initFC | boolean |  |
| initPersistentStorage | boolean |  |
| initFcStorage | boolean |  |




