# Basic Information

|      |      |
|------|------|
| Name | BloomFilterPreviewApi |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/api/data_resource/bloom_filter/BloomFilterPreviewApi.java |
| Package Name | com.welab.wefe.board.service.api.data_resource.bloom_filter |
| Dependencies | ['com.welab.wefe.board.service.constant.BloomfilterAddMethod', 'com.welab.wefe.board.service.constant.DataSetAddMethod', 'com.welab.wefe.board.service.database.entity.DataSourceMysqlModel', 'com.welab.wefe.board.service.dto.entity.data_set.DataSetColumnOutputModel', 'com.welab.wefe.board.service.service.data_resource.bloom_filter.BloomFilterService', 'com.welab.wefe.board.service.util.AbstractTableDataSetReader', 'com.welab.wefe.board.service.util.CsvTableDataSetReader', 'com.welab.wefe.board.service.util.ExcelTableDataSetReader', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.fieldvalidate.annotation.Check', 'com.welab.wefe.common.jdbc.JdbcClient', 'com.welab.wefe.common.util.ListUtil', 'com.welab.wefe.common.web.api.base.AbstractApi', 'com.welab.wefe.common.web.api.base.Api', 'com.welab.wefe.common.web.dto.AbstractApiInput', 'com.welab.wefe.common.web.dto.ApiResult', 'com.welab.wefe.common.wefe.ColumnDataTypeInferrer', 'com.welab.wefe.common.wefe.enums.ColumnDataType', 'org.apache.commons.lang3.StringUtils', 'org.springframework.beans.factory.annotation.Autowired', 'java.io.File', 'java.io.IOException', 'java.util.ArrayList', 'java.util.LinkedHashMap', 'java.util.List', 'java.util.Map', 'java.util.function.Consumer', 'java.util.regex.Pattern', 'java.util.stream.Collectors'] |
| Brief Description | The BloomFilterPreviewApi class is designed for previewing Bloom filter data, supporting data retrieval from databases or files, inferring data types, and returning metadata along with preview data. |

# Description

BloomFilterPreviewApi is an API class designed for previewing Bloom filter data, inheriting from AbstractApi. It supports reading data from databases or files and performs data type inference. Key functionalities include: validating input parameters, reading data via BloomFilterService, testing database connections, parsing CSV or Excel files, inferring data types (integer, long, double, string), and generating outputs containing headers, raw data, and metadata. The input class Input includes fields such as filename, data source ID, and SQL, while the output class Output comprises headers, raw data, and a metadata list.

# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| BloomFilterPreviewApi | class | BloomFilter Preview API, which supports reading data from databases or files, parsing data types, and generating preview results, including field lists, raw data, and metadata information. |



## Class BloomFilterPreviewApi

|      |      |
|------|------|
| Access Modifier | @Api(path = "bloom_filter/preview", name = "preview bloom_filter rows");public |
| Type | class |
| Name | BloomFilterPreviewApi |
| Description | BloomFilter Preview API, which supports reading data from databases or files, parsing data types, and generating preview results, including field lists, raw data, and metadata information. |


### UML Class Diagram

```mermaid
classDiagram
    class BloomFilterPreviewApi {
        -Pattern MATCH_INTEGER_PATTERN
        -Pattern MATCH_LONG_PATTERN
        -Pattern MATCH_DOUBLE_PATTERN
        -BloomFilterService bloomfilterService
        +handle(Input input) ApiResult~Output~
        -readFile(File file) Output
        -readFromDatabase(String dataSourceId, String sql) Output
    }

    class DataRowConsumer {
        -LinkedHashMap~String, DataSetColumnOutputModel~ metadata
        -Output output
        -boolean allColumnKnowDataType
        +DataRowConsumer(metadata, output)
        +accept(LinkedHashMap~String, Object~ x)
        -inferDataType(String value) ColumnDataType
    }

    class Input {
        -String filename
        -BloomfilterAddMethod bloomfilterAddMethod
        -String dataSourceId
        -String sql
        +checkAndStandardize()
        +get/set methods
    }

    class Output {
        -List~String~ header
        -List~Map~String, Object~~ rawDataList
        -List~DataSetColumnOutputModel~ metadataList
        +get/set methods
    }

    class DataSetColumnOutputModel {
        +String name
        +ColumnDataType dataType
        +get/set methods
    }

    class BloomFilterService {
        +testSqlQuery(String dataSourceId, String sql) String
        +getBloomfilterFile(BloomfilterAddMethod method, String filename) File
        +getDataSourceById(String dataSourceId) DataSourceMysqlModel
    }

    class JdbcClient {
        +create(databaseType, host, port, username, password, dbName) JdbcClient
        +getHeaders(String sql) List~String~
        +scan(String sql, DataRowConsumer consumer, int limit)
    }

    class AbstractTableDataSetReader {
        <<Abstract>>
        +getHeader() List~String~
        +read(DataRowConsumer consumer, int batchSize, int limit)
    }

    class CsvTableDataSetReader {
        +CsvTableDataSetReader(File file)
    }

    class ExcelTableDataSetReader {
        +ExcelTableDataSetReader(File file)
    }

    BloomFilterPreviewApi --> BloomFilterService : Dependency
    BloomFilterPreviewApi --> DataRowConsumer : Creates
    BloomFilterPreviewApi --> Input : Uses
    BloomFilterPreviewApi --> Output : Returns
    DataRowConsumer --> DataSetColumnOutputModel : Updates
    DataRowConsumer --> Output : Updates
    BloomFilterService --> DataSourceMysqlModel : Queries
    BloomFilterService --> JdbcClient : Creates
    AbstractTableDataSetReader <|-- CsvTableDataSetReader
    AbstractTableDataSetReader <|-- ExcelTableDataSetReader
    BloomFilterPreviewApi --> AbstractTableDataSetReader : Uses
```

This code implements a Bloom filter preview API, primarily functioning to read data from databases or files and infer data types. The BloomFilterPreviewApi inherits from AbstractApi, processing input parameters through the handle method and invoking readFromDatabase or readFile methods based on the data source. The DataRowConsumer class handles data rows and infers data types using regular expressions to match integers, long integers, and floating-point numbers. The BloomFilterService provides database connection and file operation services, JdbcClient executes SQL queries, and AbstractTableDataSetReader along with its subclasses are responsible for reading CSV and Excel files. The overall design adopts a layered architecture with clear responsibilities, supporting multiple data sources and file formats.


### Internal Method Call Graph

```mermaid
graph TD
    A["BloomFilterPreviewApi Class"]
    B["Property: Pattern MATCH_*_PATTERN"]
    C["Dependency: BloomFilterService"]
    D["Main Method: handle(Input input)"]
    E["Branch 1: Database Mode"]
    F["Branch 2: File Mode"]
    G["Sub-method: readFile(File file)"]
    H["Sub-method: readFromDatabase(String dataSourceId, String sql)"]
    I["Inner Class: DataRowConsumer"]
    J["Input Class: Input"]
    K["Output Class: Output"]

    A --> B
    A --> C
    A --> D
    D -->|if Database| E
    D -->|else| F
    E --> H
    F --> G
    G --> I
    H --> I
    A --> J
    A --> K
    I -->|Calls| B
```

```mermaid
sequenceDiagram
    participant Client
    participant BloomFilterPreviewApi
    participant BloomFilterService
    participant DataRowConsumer
    participant JdbcClient

    Client->>BloomFilterPreviewApi: Call handle(input)
    alt Database Mode
        BloomFilterPreviewApi->>BloomFilterService: testSqlQuery()
        BloomFilterService-->>BloomFilterPreviewApi: Return result
        BloomFilterPreviewApi->>BloomFilterPreviewApi: readFromDatabase()
        BloomFilterPreviewApi->>BloomFilterService: getDataSourceById()
        BloomFilterPreviewApi->>JdbcClient: create()
        BloomFilterPreviewApi->>JdbcClient: getHeaders()
        BloomFilterPreviewApi->>JdbcClient: scan()
        JdbcClient->>DataRowConsumer: Consume data rows
    else File Mode
        BloomFilterPreviewApi->>BloomFilterService: getBloomfilterFile()
        BloomFilterPreviewApi->>BloomFilterPreviewApi: readFile()
        activate BloomFilterPreviewApi
            BloomFilterPreviewApi->>AbstractTableDataSetReader: Create Reader
            AbstractTableDataSetReader->>DataRowConsumer: Process data
        deactivate BloomFilterPreviewApi
    end
    BloomFilterPreviewApi-->>Client: Return Output
```

This flowchart illustrates the core processing logic of BloomFilterPreviewApi, featuring two data acquisition paths: database query and file reading. The database path involves JDBC connection and SQL execution, while the file path selects CSV or Excel parsers based on extensions. The sequence diagram details the complete call chain from client request to data processing, including exception handling and data conversion. DataRowConsumer serves as the core data processing unit, responsible for data type inference and result collection, supporting a maximum 10-row data preview limit.

### Field List

| Name  | Type  | Description |
|-------|-------|------|
| MATCH_DOUBLE_PATTERN = Pattern.compile("^-?\\d+\\.\\d+$") | Pattern | Define a static constant MATCH_DOUBLE_PATTERN for matching floating-point number formats with optional negative signs. |
| bloomfilterService | BloomFilterService | Automatically inject the Bloom filter service instance. |
| MATCH_INTEGER_PATTERN = Pattern.compile("^-?\\d{1,9}$") | Pattern | Define a static constant integer matching regex pattern to check for optional negative sign integers with 1 to 9 digits. |
| MATCH_LONG_PATTERN = Pattern.compile("^-?\\d{10,}$") | Pattern | Define a static constant MATCH_LONG_PATTERN, using a regular expression to match 10 or more digits, allowing a leading negative sign. |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| handle | ApiResult<Output> | The method selects the data source based on the input: if it is a database, it tests the SQL connection and reads the data, throwing an exception if it fails; if it is a file, it reads the file content, logs errors and throws a system error if any issues occur. Finally, it returns the processing result. |
| readFile | Output | The method `readFile` reads file data, processes the first row as column headers and the remaining rows as data rows, supports CSV and Excel formats, and returns an `Output` object containing metadata and content. |
| readFromDatabase | Output | Methods for reading data from a database: Retrieve the data source configuration based on the dataSourceId, establish a JDBC connection, and execute an SQL query. Check for duplicate column names, convert 'Y' to 'y', and if a 'y' column exists, move it to the second column. Construct an output object containing column names and metadata, process the data rows through a consumer, and return the result. |




