# Basic Information

|      |      |
|------|------|
| Name | CaCertificateCache |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/cache/CaCertificateCache.java |
| Package Name | com.welab.wefe.board.service.cache |
| Dependencies | ['com.welab.wefe.board.service.sdk.union.UnionService', 'com.welab.wefe.common.web.Launcher', 'org.apache.commons.collections4.CollectionUtils', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.util.ArrayList', 'java.util.List', 'java.util.concurrent.ConcurrentHashMap'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| CaCertificateCache | class |  |



## Class CaCertificateCache

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | CaCertificateCache |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| LOG = LoggerFactory.getLogger(CaCertificateCache.class) | Logger |  |
| caCertificateCache = new CaCertificateCache() | CaCertificateCache |  |
| data = new ConcurrentHashMap<>() | ConcurrentHashMap<String, CaCertificate> |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| refreshCache | boolean |  |
| getInstance | CaCertificateCache |  |
| get | CaCertificate |  |
| getAll | List<CaCertificate> |  |




