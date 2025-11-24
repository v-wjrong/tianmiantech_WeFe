# 基础信息

|      |      |
|------|------|
| 名称 | SystemConfigCache |
| 编码语言 | .java |
| 代码路径 | WeFe/gateway/src/main/java/com/welab/wefe/gateway/cache/SystemConfigCache.java |
| 包名 | com.welab.wefe.gateway.cache |
| 依赖项 | ['com.welab.wefe.common.util.IpAddressUtil', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.wefe.dto.global_config.GatewayConfigModel', 'com.welab.wefe.gateway.GatewayServer', 'com.welab.wefe.gateway.service.GlobalConfigService', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.util.CollectionUtils', 'java.util.ArrayList', 'java.util.List', 'java.util.concurrent.ConcurrentSkipListSet'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| SystemConfigCache | class |  |



## 类 SystemConfigCache

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | SystemConfigCache |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| LOG = LoggerFactory.getLogger(SystemConfigCache.class) | Logger |  |
| IP_ADDRESS_LIST = new ConcurrentSkipListSet<>() | ConcurrentSkipListSet<String> |  |
| cache = new SystemConfigCache() | SystemConfigCache |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getInstance | SystemConfigCache |  |
| isExistIp | boolean |  |
| cacheIsEmpty | boolean |  |
| refreshCache | boolean |  |




