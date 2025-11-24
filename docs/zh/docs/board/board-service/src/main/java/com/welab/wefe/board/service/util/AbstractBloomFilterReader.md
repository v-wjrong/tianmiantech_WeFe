# 基础信息

|      |      |
|------|------|
| 名称 | AbstractBloomFilterReader |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/util/AbstractBloomFilterReader.java |
| 包名 | com.welab.wefe.board.service.util |
| 依赖项 | ['com.welab.wefe.board.service.dto.fusion.BloomFilterColumnInputModel', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'java.io.Closeable', 'java.util.LinkedHashMap', 'java.util.List', 'java.util.Map', 'java.util.function.Consumer', 'java.util.stream.Collectors'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| AbstractBloomFilterReader | class |  |



## 类 AbstractBloomFilterReader

|      |      |
|------|------|
| 访问范围 | public abstract |
| 类型 | class |
| 名称 | AbstractBloomFilterReader |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| metadataMap | Map<String, BloomFilterColumnInputModel> |  |
| containsY | boolean |  |
| header | List<String> |  |
| readDataRows = 0 | int |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getReadDataRows | long |  |
| isContainsY | boolean |  |
| read | void |  |
| getHeader | List<String> |  |
| readAll | void |  |
| doGetHeader | List<String> |  |
| getTotalDataRowCount | long |  |
| readOneRow | LinkedHashMap<String, Object> |  |




