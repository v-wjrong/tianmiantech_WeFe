# 基础信息

|      |      |
|------|------|
| 名称 | CsvTableDataSetReader |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/util/CsvTableDataSetReader.java |
| 包名 | com.welab.wefe.board.service.util |
| 依赖项 | ['com.welab.wefe.board.service.dto.entity.data_set.DataSetColumnInputModel', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'de.siegmar.fastcsv.reader.CsvParser', 'de.siegmar.fastcsv.reader.CsvReader', 'de.siegmar.fastcsv.reader.CsvRow', 'java.io.File', 'java.io.FileReader', 'java.io.IOException', 'java.io.LineNumberReader', 'java.nio.charset.StandardCharsets', 'java.util.LinkedHashMap', 'java.util.List'] |
| 概述说明 | CsvTableDataSetReader类继承AbstractTableDataSetReader，用于读取CSV文件数据。包含获取表头、计算总行数、逐行读取数据及关闭解析器功能。支持自定义元数据和UTF-8编码。 |

# 说明

CsvTableDataSetReader是一个继承自AbstractTableDataSetReader的类，用于读取CSV文件数据。它包含一个CsvParser解析器、文件对象和行数计数器。构造函数支持传入文件路径和元数据列表，初始化时配置CSV读取器跳过空行和表头。方法包括获取表头、计算总行数、逐行读取数据到LinkedHashMap以及关闭解析器。总行数通过文件行号统计，读取失败时抛出异常。

# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| CsvTableDataSetReader | class | CsvTableDataSetReader类继承AbstractTableDataSetReader，用于读取CSV文件数据。构造函数初始化CSV解析器，支持无表头模式。方法包括获取表头、计算总行数、逐行读取数据到LinkedHashMap及关闭解析器。异常处理完善。 |



## 类 CsvTableDataSetReader

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | CsvTableDataSetReader |
| 说明 | CsvTableDataSetReader类继承AbstractTableDataSetReader，用于读取CSV文件数据。构造函数初始化CSV解析器，支持无表头模式。方法包括获取表头、计算总行数、逐行读取数据到LinkedHashMap及关闭解析器。异常处理完善。 |


### UML类图

```mermaid
classDiagram
    class AbstractTableDataSetReader {
        <<Abstract>>
        #List~String~ header
        #long readDataRows
        +AbstractTableDataSetReader(List~DataSetColumnInputModel~ metadataList)
        +List~String~ getHeader()
        +long getTotalDataRowCount()
        #List~String~ doGetHeader() throws Exception
        #LinkedHashMap~String, Object~ readOneRow() throws StatusCodeWithException
        +void close() throws IOException
    }

    class CsvTableDataSetReader {
        -CsvParser parser
        -long totalRowCount
        -File file
        +CsvTableDataSetReader(File file) throws IOException
        +CsvTableDataSetReader(List~DataSetColumnInputModel~ metadataList, File file) throws IOException
        #List~String~ doGetHeader() throws Exception
        +long getTotalDataRowCount()
        #LinkedHashMap~String, Object~ readOneRow() throws StatusCodeWithException
        +void close() throws IOException
    }

    class CsvParser {
        <<Interface>>
        +CsvRow nextRow()
        +void close()
    }

    class CsvRow {
        <<Interface>>
        +List~String~ getFields()
        +int getFieldCount()
        +String getField(int index)
    }

    class StatusCodeWithException {
        +StatusCode statusCode
        +String message
        +StatusCodeWithException(StatusCode statusCode, String message)
    }

    AbstractTableDataSetReader <|-- CsvTableDataSetReader
    CsvTableDataSetReader --> CsvParser : 使用
    CsvTableDataSetReader --> CsvRow : 解析
    CsvTableDataSetReader --> StatusCodeWithException : 抛出异常
    CsvParser ..> CsvRow : 生成
```

该代码实现了一个CSV表格数据读取器，继承自抽象表格读取器。主要功能包括解析CSV文件头、计算总行数、逐行读取数据，并处理可能的异常情况。类图展示了继承关系、接口实现和关键依赖，其中CsvParser和CsvRow为接口，StatusCodeWithException是自定义异常类。读取器通过组合方式使用CSV解析器，同时实现了抽象类定义的四个核心方法。


### 内部方法调用关系图

```mermaid
graph TD
    A["类CsvTableDataSetReader"]
    B["属性: CsvParser parser"]
    C["属性: long totalRowCount"]
    D["属性: File file"]
    E["构造方法: CsvTableDataSetReader(File file)"]
    F["构造方法: CsvTableDataSetReader(List<DataSetColumnInputModel> metadataList, File file)"]
    G["方法: List<String> doGetHeader()"]
    H["方法: long getTotalDataRowCount()"]
    I["方法: LinkedHashMap<String, Object> readOneRow()"]
    J["方法: void close()"]
    K["内部操作: 初始化CsvReader并解析文件"]
    L["内部操作: 读取CSV行并返回字段列表"]
    M["内部操作: 计算文件总行数"]
    N["内部操作: 读取单行数据并映射到LinkedHashMap"]
    O["内部操作: 关闭parser"]

    A --> B
    A --> C
    A --> D
    A --> E
    A --> F
    A --> G
    A --> H
    A --> I
    A --> J
    E --> F
    F --> K
    G --> L
    H --> M
    I --> N
    J --> O
```

该流程图展示了CsvTableDataSetReader类的完整结构，包含4个主要方法和2个构造方法。核心功能包括CSV文件解析、表头获取、行数统计、数据行读取和资源释放。构造方法会初始化CSV解析器，doGetHeader()读取首行作为表头，getTotalDataRowCount()通过行号统计计算总行数，readOneRow()将每行数据映射到有序字典，close()负责关闭解析器释放资源。

### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| parser | CsvParser | 私有不可变的CSV解析器实例。 |
| totalRowCount | long | 私有长整型变量，记录总行数。 |
| file | File | 私有不可变文件对象。 |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| doGetHeader | List<String> | 重写doGetHeader方法，解析CSV下一行并返回字段列表。 |
| getTotalDataRowCount | long | 方法getTotalDataRowCount返回文件行数。若totalRowCount已缓存则直接返回，否则读取文件计算行数并缓存结果。异常时返回0。 |
| readOneRow | LinkedHashMap<String, Object> | 方法readOneRow读取CSV一行数据，转为LinkedHashMap。若行空返回null，否则按表头映射字段值。出错抛异常提示行号和错误信息。 |
| close | void | Java方法重写，关闭解析器并可能抛出IO异常。 |




