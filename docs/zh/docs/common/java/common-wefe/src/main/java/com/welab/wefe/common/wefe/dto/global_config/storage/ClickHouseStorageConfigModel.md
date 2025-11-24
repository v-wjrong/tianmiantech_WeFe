# 基础信息

|      |      |
|------|------|
| 名称 | ClickHouseStorageConfigModel |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-wefe/src/main/java/com/welab/wefe/common/wefe/dto/global_config/storage/ClickHouseStorageConfigModel.java |
| 包名 | com.welab.wefe.common.wefe.dto.global_config.storage |
| 依赖项 | ['com.welab.wefe.common.wefe.dto.global_config.base.AbstractConfigModel', 'com.welab.wefe.common.wefe.dto.global_config.base.ConfigGroupConstant', 'com.welab.wefe.common.wefe.dto.global_config.base.ConfigModel', 'com.welab.wefe.common.fieldvalidate.secret.MaskStrategy', 'com.welab.wefe.common.fieldvalidate.secret.Secret', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.wefe.dto.storage.ClickhouseConfig'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| ClickHouseStorageConfigModel | class |  |



## 类 ClickHouseStorageConfigModel

|      |      |
|------|------|
| 访问范围 | @ConfigModel(group = ConfigGroupConstant.CLICKHOUSE_STORAGE);public |
| 类型 | class |
| 名称 | ClickHouseStorageConfigModel |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| username | String |  |
| password | String |  |
| host | String |  |
| tcpPort = 9000 | int |  |
| http_port = 8123 | int |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| toStorageConfig | ClickhouseConfig |  |




