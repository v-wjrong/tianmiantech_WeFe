# Basic Information

|      |      |
|------|------|
| Name | CsvTableDataSetReader |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/util/CsvTableDataSetReader.java |
| Package Name | com.welab.wefe.board.service.util |
| Dependencies | ['com.welab.wefe.board.service.dto.entity.data_set.DataSetColumnInputModel', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'de.siegmar.fastcsv.reader.CsvParser', 'de.siegmar.fastcsv.reader.CsvReader', 'de.siegmar.fastcsv.reader.CsvRow', 'java.io.File', 'java.io.FileReader', 'java.io.IOException', 'java.io.LineNumberReader', 'java.nio.charset.StandardCharsets', 'java.util.LinkedHashMap', 'java.util.List'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| CsvTableDataSetReader | class |  |



## Class CsvTableDataSetReader

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | CsvTableDataSetReader |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| file | File |  |
| parser | CsvParser |  |
| totalRowCount | long |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getTotalDataRowCount | long |  |
| doGetHeader | List<String> |  |
| readOneRow | LinkedHashMap<String, Object> |  |
| close | void |  |




