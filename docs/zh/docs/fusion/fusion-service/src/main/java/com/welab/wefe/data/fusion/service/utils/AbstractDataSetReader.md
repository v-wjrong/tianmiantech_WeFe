# 基础信息

|      |      |
|------|------|
| 名称 | AbstractDataSetReader |
| 编码语言 | .java |
| 代码路径 | WeFe/fusion/fusion-service/src/main/java/com/welab/wefe/data/fusion/service/utils/AbstractDataSetReader.java |
| 包名 | com.welab.wefe.data.fusion.service.utils |
| 依赖项 | ['com.welab.wefe.common.CommonThreadPool', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'java.io.Closeable', 'java.io.IOException', 'java.util.ArrayList', 'java.util.LinkedHashMap', 'java.util.List', 'java.util.Map', 'java.util.function.Consumer', 'java.util.stream.Collectors'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| AbstractDataSetReader | class |  |



## 类 AbstractDataSetReader

|      |      |
|------|------|
| 访问范围 | public abstract |
| 类型 | class |
| 名称 | AbstractDataSetReader |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| readDataRows = 0 | int |  |
| containsY | boolean |  |
| header | List<String> |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| isContainsY | boolean |  |
| readWithSelectRow | void |  |
| readAllWithSelectRow | void |  |
| readWithSelectRow | void |  |
| getHeader | List<String> |  |
| readOneRow | LinkedHashMap<String, Object> |  |
| getHeader | List<String> |  |
| getReadDataRows | int |  |
| read | void |  |
| doGetHeader | List<String> |  |
| readAll | void |  |
| getRowCount | long |  |




