# 基础信息

|      |      |
|------|------|
| 名称 | ExcelReader |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-lang/src/main/java/com/welab/wefe/common/io/excel/ExcelReader.java |
| 包名 | com.welab.wefe.common.io.excel |
| 依赖项 | ['com.alibaba.fastjson.util.TypeUtils', 'com.welab.wefe.common.util.StringUtil', 'org.apache.poi.ss.usermodel', 'java.io.Closeable', 'java.io.File', 'java.io.IOException', 'java.io.InputStream', 'java.util.ArrayList', 'java.util.LinkedHashMap', 'java.util.List', 'java.util.Map', 'java.util.function.Consumer', 'java.util.stream.Collectors'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| ExcelReader | class |  |



## 类 ExcelReader

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | ExcelReader |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| workbook | Workbook |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| readSheetWithTitleRow | void |  |
| getColumnNames | List<String> |  |
| getSheetCount | int |  |
| getRowData | List<Object> |  |
| getRowDataWithoutLastEmptyCell | List<Object> |  |
| getColumnCount | int |  |
| getRowCount | long |  |
| getWorkbook | Workbook |  |
| readSheetWithoutTitleRow | void |  |
| getSheet | Sheet |  |
| getSheet | Sheet |  |
| readSheetWithTitleRow | void |  |
| getCellValue | Object |  |
| close | void |  |




