# 基础信息

|      |      |
|------|------|
| 名称 | CaCertificateCache |
| 编码语言 | .java |
| 代码路径 | WeFe/gateway/src/main/java/com/welab/wefe/gateway/cache/CaCertificateCache.java |
| 包名 | com.welab.wefe.gateway.cache |
| 依赖项 | ['com.welab.wefe.gateway.GatewayServer', 'com.welab.wefe.gateway.service.CaCertificateService', 'org.apache.commons.collections4.CollectionUtils', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.util.ArrayList', 'java.util.List', 'java.util.concurrent.ConcurrentHashMap'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| CaCertificateCache | class |  |



## 类 CaCertificateCache

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | CaCertificateCache |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| LOG = LoggerFactory.getLogger(CaCertificateCache.class) | Logger |  |
| data = new ConcurrentHashMap<>() | ConcurrentHashMap<String, CaCertificate> |  |
| caCertificateCache = new CaCertificateCache() | CaCertificateCache |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getInstance | CaCertificateCache |  |
| refreshCache | boolean |  |
| get | CaCertificate |  |
| getAll | List<CaCertificate> |  |




