# Basic Information

|      |      |
|------|------|
| Name | SqlTableDataSetReader |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/util/SqlTableDataSetReader.java |
| Package Name | com.welab.wefe.board.service.util |
| Dependencies | ['com.welab.wefe.board.service.dto.entity.data_set.DataSetColumnInputModel', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.jdbc.JdbcClient', 'com.welab.wefe.common.jdbc.base.JdbcScanner', 'org.apache.commons.collections4.CollectionUtils', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.io.IOException', 'java.util.LinkedHashMap', 'java.util.List'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| SqlTableDataSetReader | class |  |



## Class SqlTableDataSetReader

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | SqlTableDataSetReader |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| sql | String |  |
| LOG = LoggerFactory.getLogger(SqlTableDataSetReader.class) | Logger |  |
| jdbcClient | JdbcClient |  |
| scanner | JdbcScanner |  |
| totalRowCount = -1 | long |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| close | void |  |
| readOneRow | LinkedHashMap<String, Object> |  |
| doGetHeader | List<String> |  |
| getTotalDataRowCount | long |  |




