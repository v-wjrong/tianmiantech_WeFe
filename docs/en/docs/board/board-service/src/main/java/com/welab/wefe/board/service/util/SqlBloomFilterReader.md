# Basic Information

|      |      |
|------|------|
| Name | SqlBloomFilterReader |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/util/SqlBloomFilterReader.java |
| Package Name | com.welab.wefe.board.service.util |
| Dependencies | ['com.welab.wefe.board.service.dto.fusion.BloomFilterColumnInputModel', 'com.welab.wefe.common.jdbc.JdbcClient', 'com.welab.wefe.common.jdbc.base.JdbcScanner', 'org.apache.commons.collections4.CollectionUtils', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.io.IOException', 'java.util.LinkedHashMap', 'java.util.List'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| SqlBloomFilterReader | class |  |



## Class SqlBloomFilterReader

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | SqlBloomFilterReader |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| totalRowCount = -1 | long |  |
| jdbcClient | JdbcClient |  |
| sql | String |  |
| scanner | JdbcScanner |  |
| headers | List<String> |  |
| LOG = LoggerFactory.getLogger(SqlBloomFilterReader.class) | Logger |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| readOneRow | LinkedHashMap<String, Object> |  |
| getTotalDataRowCount | long |  |
| doGetHeader | List<String> |  |
| close | void |  |




