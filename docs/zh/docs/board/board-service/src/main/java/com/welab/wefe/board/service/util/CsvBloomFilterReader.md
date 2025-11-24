# 基础信息

|      |      |
|------|------|
| 名称 | CsvBloomFilterReader |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/util/CsvBloomFilterReader.java |
| 包名 | com.welab.wefe.board.service.util |
| 依赖项 | ['com.welab.wefe.board.service.dto.fusion.BloomFilterColumnInputModel', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'de.siegmar.fastcsv.reader.CsvParser', 'de.siegmar.fastcsv.reader.CsvReader', 'de.siegmar.fastcsv.reader.CsvRow', 'java.io.File', 'java.io.FileReader', 'java.io.IOException', 'java.io.LineNumberReader', 'java.nio.charset.StandardCharsets', 'java.util.LinkedHashMap', 'java.util.List'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| CsvBloomFilterReader | class |  |



## 类 CsvBloomFilterReader

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | CsvBloomFilterReader |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| totalRowCount | long |  |
| parser | CsvParser |  |
| file | File |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| close | void |  |
| getTotalDataRowCount | long |  |
| doGetHeader | List<String> |  |
| readOneRow | LinkedHashMap<String, Object> |  |




