# Basic Information

|      |      |
|------|------|
| Name | SystemConfigCache |
| Language | .java |
| Code Path | WeFe/gateway/src/main/java/com/welab/wefe/gateway/cache/SystemConfigCache.java |
| Package Name | com.welab.wefe.gateway.cache |
| Dependencies | ['com.welab.wefe.common.util.IpAddressUtil', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.wefe.dto.global_config.GatewayConfigModel', 'com.welab.wefe.gateway.GatewayServer', 'com.welab.wefe.gateway.service.GlobalConfigService', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.util.CollectionUtils', 'java.util.ArrayList', 'java.util.List', 'java.util.concurrent.ConcurrentSkipListSet'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| SystemConfigCache | class |  |



## Class SystemConfigCache

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | SystemConfigCache |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| LOG = LoggerFactory.getLogger(SystemConfigCache.class) | Logger |  |
| IP_ADDRESS_LIST = new ConcurrentSkipListSet<>() | ConcurrentSkipListSet<String> |  |
| cache = new SystemConfigCache() | SystemConfigCache |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getInstance | SystemConfigCache |  |
| isExistIp | boolean |  |
| cacheIsEmpty | boolean |  |
| refreshCache | boolean |  |




