# Basic Information

|      |      |
|------|------|
| Name | ClassPathScanHandler |
| Language | .java |
| Code Path | WeFe/union/blockchain-data-sync/src/main/java/com/welab/wefe/tool/ClassPathScanHandler.java |
| Package Name | com.welab.wefe.tool |
| Dependencies | ['org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.io.File', 'java.io.IOException', 'java.net.JarURLConnection', 'java.net.URL', 'java.net.URLDecoder', 'java.util.Enumeration', 'java.util.LinkedHashSet', 'java.util.List', 'java.util.Set', 'java.util.jar.JarEntry', 'java.util.jar.JarFile', 'java.util.regex.Pattern'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| ClassPathScanHandler | class |  |



## Class ClassPathScanHandler

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | ClassPathScanHandler |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| classFilters = null | List<String> |  |
| log = LoggerFactory.getLogger(ClassPathScanHandler.class) | Logger |  |
| excludeInner = true | boolean |  |
| checkInOrEx = true | boolean |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| setClassFilters | void |  |
| isCheckInOrEx | boolean |  |
| filterClassName | boolean |  |
| getPackageAllClasses | Set<Class<?>> |  |
| setExcludeInner | void |  |
| getClassFilters | List<String> |  |
| isExcludeInner | boolean |  |
| setCheckInOrEx | void |  |
| doScanPackageClassesByJar | void |  |
| doScanPackageClassesByFile | void |  |




