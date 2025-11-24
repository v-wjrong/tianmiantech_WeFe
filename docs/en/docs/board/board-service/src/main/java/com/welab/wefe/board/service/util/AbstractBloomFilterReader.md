# Basic Information

|      |      |
|------|------|
| Name | AbstractBloomFilterReader |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/util/AbstractBloomFilterReader.java |
| Package Name | com.welab.wefe.board.service.util |
| Dependencies | ['com.welab.wefe.board.service.dto.fusion.BloomFilterColumnInputModel', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'java.io.Closeable', 'java.util.LinkedHashMap', 'java.util.List', 'java.util.Map', 'java.util.function.Consumer', 'java.util.stream.Collectors'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| AbstractBloomFilterReader | class |  |



## Class AbstractBloomFilterReader

|      |      |
|------|------|
| Access Modifier | public abstract |
| Type | class |
| Name | AbstractBloomFilterReader |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| metadataMap | Map<String, BloomFilterColumnInputModel> |  |
| containsY | boolean |  |
| header | List<String> |  |
| readDataRows = 0 | int |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getReadDataRows | long |  |
| isContainsY | boolean |  |
| read | void |  |
| getHeader | List<String> |  |
| readAll | void |  |
| doGetHeader | List<String> |  |
| getTotalDataRowCount | long |  |
| readOneRow | LinkedHashMap<String, Object> |  |




