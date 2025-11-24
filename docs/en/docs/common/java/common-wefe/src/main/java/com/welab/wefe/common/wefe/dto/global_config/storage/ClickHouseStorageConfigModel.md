# Basic Information

|      |      |
|------|------|
| Name | ClickHouseStorageConfigModel |
| Language | .java |
| Code Path | WeFe/common/java/common-wefe/src/main/java/com/welab/wefe/common/wefe/dto/global_config/storage/ClickHouseStorageConfigModel.java |
| Package Name | com.welab.wefe.common.wefe.dto.global_config.storage |
| Dependencies | ['com.welab.wefe.common.wefe.dto.global_config.base.AbstractConfigModel', 'com.welab.wefe.common.wefe.dto.global_config.base.ConfigGroupConstant', 'com.welab.wefe.common.wefe.dto.global_config.base.ConfigModel', 'com.welab.wefe.common.fieldvalidate.secret.MaskStrategy', 'com.welab.wefe.common.fieldvalidate.secret.Secret', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.wefe.dto.storage.ClickhouseConfig'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| ClickHouseStorageConfigModel | class |  |



## Class ClickHouseStorageConfigModel

|      |      |
|------|------|
| Access Modifier | @ConfigModel(group = ConfigGroupConstant.CLICKHOUSE_STORAGE);public |
| Type | class |
| Name | ClickHouseStorageConfigModel |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| username | String |  |
| password | String |  |
| host | String |  |
| tcpPort = 9000 | int |  |
| http_port = 8123 | int |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| toStorageConfig | ClickhouseConfig |  |




