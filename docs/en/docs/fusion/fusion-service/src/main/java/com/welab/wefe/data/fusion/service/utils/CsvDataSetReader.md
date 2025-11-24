# Basic Information

|      |      |
|------|------|
| Name | CsvDataSetReader |
| Language | .java |
| Code Path | WeFe/fusion/fusion-service/src/main/java/com/welab/wefe/data/fusion/service/utils/CsvDataSetReader.java |
| Package Name | com.welab.wefe.data.fusion.service.utils |
| Dependencies | ['com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'de.siegmar.fastcsv.reader.CsvParser', 'de.siegmar.fastcsv.reader.CsvReader', 'de.siegmar.fastcsv.reader.CsvRow', 'java.io.File', 'java.io.IOException', 'java.nio.charset.StandardCharsets', 'java.util.LinkedHashMap', 'java.util.List'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| CsvDataSetReader | class |  |



## Class CsvDataSetReader

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | CsvDataSetReader |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| parser | CsvParser |  |
| reader = new CsvReader() | CsvReader |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| doGetHeader | List<String> |  |
| close | void |  |
| readOneRow | LinkedHashMap<String, Object> |  |
| getRowCount | long |  |




