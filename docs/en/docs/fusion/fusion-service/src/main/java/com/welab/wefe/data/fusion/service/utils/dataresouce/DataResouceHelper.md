# Basic Information

|      |      |
|------|------|
| Name | DataResouceHelper |
| Language | .java |
| Code Path | WeFe/fusion/fusion-service/src/main/java/com/welab/wefe/data/fusion/service/utils/dataresouce/DataResouceHelper.java |
| Package Name | com.welab.wefe.data.fusion.service.utils.dataresouce |
| Dependencies | ['com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.web.Launcher', 'com.welab.wefe.common.wefe.enums.ColumnDataType', 'com.welab.wefe.data.fusion.service.database.entity.DataSetColumnOutputModel', 'com.welab.wefe.data.fusion.service.database.entity.DataSourceMySqlModel', 'com.welab.wefe.data.fusion.service.dto.entity.dataset.DataSetPreviewOutputModel', 'com.welab.wefe.data.fusion.service.manager.JdbcManager', 'com.welab.wefe.data.fusion.service.service.DataSourceService', 'com.welab.wefe.data.fusion.service.utils.AbstractDataSetReader', 'com.welab.wefe.data.fusion.service.utils.CsvDataSetReader', 'com.welab.wefe.data.fusion.service.utils.ExcelDataSetReader', 'java.io.File', 'java.io.IOException', 'java.sql.Connection', 'java.util.ArrayList', 'java.util.LinkedHashMap', 'java.util.List', 'java.util.Map', 'java.util.function.Consumer', 'java.util.regex.Pattern', 'java.util.stream.Collectors'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| DataResouceHelper | class |  |



## Class DataResouceHelper

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | DataResouceHelper |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| MATCH_DOUBLE_PATTERN = Pattern.compile("^-?\\d+\\.\\d+$") | Pattern |  |
| MATCH_LONG_PATTERN = Pattern.compile("^-?\\d{10,}$") | Pattern |  |
| MATCH_INTEGER_PATTERN = Pattern.compile("^-?\\d{1,9}$") | Pattern |  |
| dataSourceService | DataSourceService |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| readFile | DataSetPreviewOutputModel |  |
| readFile | DataSetPreviewOutputModel |  |
| readFromDB | DataSetPreviewOutputModel |  |
| readFromSourceDB | DataSetPreviewOutputModel |  |




