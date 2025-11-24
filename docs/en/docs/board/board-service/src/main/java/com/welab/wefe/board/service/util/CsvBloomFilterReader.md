# Basic Information

|      |      |
|------|------|
| Name | CsvBloomFilterReader |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/util/CsvBloomFilterReader.java |
| Package Name | com.welab.wefe.board.service.util |
| Dependencies | ['com.welab.wefe.board.service.dto.fusion.BloomFilterColumnInputModel', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'de.siegmar.fastcsv.reader.CsvParser', 'de.siegmar.fastcsv.reader.CsvReader', 'de.siegmar.fastcsv.reader.CsvRow', 'java.io.File', 'java.io.FileReader', 'java.io.IOException', 'java.io.LineNumberReader', 'java.nio.charset.StandardCharsets', 'java.util.LinkedHashMap', 'java.util.List'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| CsvBloomFilterReader | class |  |



## Class CsvBloomFilterReader

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | CsvBloomFilterReader |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| totalRowCount | long |  |
| parser | CsvParser |  |
| file | File |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| close | void |  |
| getTotalDataRowCount | long |  |
| doGetHeader | List<String> |  |
| readOneRow | LinkedHashMap<String, Object> |  |




