# 基础信息

|      |      |
|------|------|
| 名称 | ClassPathScanHandler |
| 编码语言 | .java |
| 代码路径 | WeFe/union/blockchain-data-sync/src/main/java/com/welab/wefe/tool/ClassPathScanHandler.java |
| 包名 | com.welab.wefe.tool |
| 依赖项 | ['org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.io.File', 'java.io.IOException', 'java.net.JarURLConnection', 'java.net.URL', 'java.net.URLDecoder', 'java.util.Enumeration', 'java.util.LinkedHashSet', 'java.util.List', 'java.util.Set', 'java.util.jar.JarEntry', 'java.util.jar.JarFile', 'java.util.regex.Pattern'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| ClassPathScanHandler | class |  |



## 类 ClassPathScanHandler

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | ClassPathScanHandler |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| classFilters = null | List<String> |  |
| log = LoggerFactory.getLogger(ClassPathScanHandler.class) | Logger |  |
| excludeInner = true | boolean |  |
| checkInOrEx = true | boolean |  |

### 方法列表

| 名称  | 类型  | 说明 |
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




