# 基础信息

|      |      |
|------|------|
| 名称 | PartnerConfigCache |
| 编码语言 | .java |
| 代码路径 | WeFe/gateway/src/main/java/com/welab/wefe/gateway/cache/PartnerConfigCache.java |
| 包名 | com.welab.wefe.gateway.cache |
| 依赖项 | ['com.welab.wefe.gateway.GatewayServer', 'com.welab.wefe.gateway.entity.PartnerConfigEntity', 'com.welab.wefe.gateway.service.PartnerConfigService', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.util.CollectionUtils', 'java.util.ArrayList', 'java.util.List', 'java.util.concurrent.ConcurrentHashMap'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| PartnerConfigCache | class |  |



## 类 PartnerConfigCache

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | PartnerConfigCache |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| partnerConfigCache = new PartnerConfigCache() | PartnerConfigCache |  |
| LOG = LoggerFactory.getLogger(PartnerConfigCache.class) | Logger |  |
| data = new ConcurrentHashMap<>() | ConcurrentHashMap<String, PartnerConfigEntity> |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getInstance | PartnerConfigCache |  |
| get | PartnerConfigEntity |  |
| refreshCache | boolean |  |




