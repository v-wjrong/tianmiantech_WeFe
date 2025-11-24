# Basic Information

|      |      |
|------|------|
| Name | PartnerConfigCache |
| Language | .java |
| Code Path | WeFe/gateway/src/main/java/com/welab/wefe/gateway/cache/PartnerConfigCache.java |
| Package Name | com.welab.wefe.gateway.cache |
| Dependencies | ['com.welab.wefe.gateway.GatewayServer', 'com.welab.wefe.gateway.entity.PartnerConfigEntity', 'com.welab.wefe.gateway.service.PartnerConfigService', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.util.CollectionUtils', 'java.util.ArrayList', 'java.util.List', 'java.util.concurrent.ConcurrentHashMap'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| PartnerConfigCache | class |  |



## Class PartnerConfigCache

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | PartnerConfigCache |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| partnerConfigCache = new PartnerConfigCache() | PartnerConfigCache |  |
| LOG = LoggerFactory.getLogger(PartnerConfigCache.class) | Logger |  |
| data = new ConcurrentHashMap<>() | ConcurrentHashMap<String, PartnerConfigEntity> |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getInstance | PartnerConfigCache |  |
| get | PartnerConfigEntity |  |
| refreshCache | boolean |  |




